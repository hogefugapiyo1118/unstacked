# Node.js dev base for creating a Next.js project inside the container
FROM node:22-bookworm-slim

ENV DEBIAN_FRONTEND=noninteractive

# Useful CLI tools for development and Git-based workflows
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    git \
    ca-certificates \
    openssh-client \
    && rm -rf /var/lib/apt/lists/*

# Workdir owned by the non-root "node" user
WORKDIR /workspace
RUN chown -R node:node /workspace
USER node

# Next.js dev server port
EXPOSE 3000

# Keep the container running in dev; VS Code will start tasks/commands
CMD ["sleep", "infinity"]
