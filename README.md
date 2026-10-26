#!/usr/bin/env bash
set -euo pipefail

mkdir -p .github/workflows \
  backend/src/config backend/src/controllers backend/src/middleware \
  backend/src/models backend/src/routes backend/src/scripts backend/src/services \
  backend/src/types backend/src/utils \
  frontend/src/pages

git init
git checkout -b feature/matrix-ai-content-engine

cat > .gitignore <<'EOF'
node_modules
dist
build
coverage
.env
.env.*
!.env.example
.DS_Store
npm-debug.log*
yarn-debug.log*
yarn-error.log*
EOF

cat > .env.example <<'EOF'
NODE_ENV=development
PORT=5000
MONGODB_URI=mongodb://localhost:27017/matrix
JWT_SECRET=super_secret_change_this
OPENAI_API_KEY=your_openai_api_key
CLIENT_URL=http://localhost:5173
EOF

cat > docker-compose.yml <<'EOF'
version: "3.9"

services:
  mongo:
    image: mongo:7
    container_name: matrix-mongo
    restart: unless-stopped
    ports:
      - "27017:27017"
    environment:
      MONGO_INITDB_DATABASE: matrix
    volumes:
      - mongo_data:/data/db

volumes:
  mongo_data:
EOF

cat > README.md <<'EOF'
# MATRIX AI Content Engine

A workspace-bound AI content generation platform for product-driven content creation and automation.

## Features
- Workspace-bound multi-tenant generation
- Product-based AI copy generation
- Supported content types:
  - description
  - review
  - seo
  - social
  - ad
- OpenAI-powered generation
- JWT auth
- Role enforcement:
  - owner
  - admin
  - editor
  - viewer
- Login + registration UI
- Premium SaaS dashboard
- Usage metering hooks
- MongoDB integration
- Docker + CI

## Setup

### 1) Install dependencies
```bash
npm --prefix backend install
npm --prefix frontend install