# ⚙️ ChainForge v4 — *Living Relics + Forge of Wisdom*

> *“Every flame remembers its source.”*

ChainForge v4 introduces **dynamic NFT relics** whose form and value evolve through player actions.  
Each quest, decision, or pulse inside the Forge alters on-chain metadata, powered by $CHAIN economy.

---

### 🚀 Features
- 🧭 **Forge of Wisdom Cinematic** → autoplays on launch  
- 💠 **Living Relics System** — NFTs gain XP, attunement, and visual tiers  
- 🔗 **Polygon Amoy Integration** (low-gas testnet)  
- 🪙 **$CHAIN Economy** — stake, burn, and reward loops  
- 🧠 **Memory Core** — tracks Light / Neutral / Dark resonance  
- 🖥️ **React HUD** with Bonding Panel + Forge Heart metrics  

---

### 🧩 Stack
| Layer | Tech |
|:--|:--|
| Contracts | Solidity + EIP-4906 |
| Backend | Fastify + Prisma + PostgreSQL |
| Worker | TypeScript heartbeat processor |
| Front-end | React + Vite |
| Network | Polygon Amoy |
| Infra | Docker + Redis + Postgres |

---

### ⚙️ Local Setup
```bash
docker compose up -d
cd apps/api && cp .env.example .env
pnpm i && pnpm prisma:dev && pnpm dev
cd ../worker && pnpm i && pnpm dev
cd ../web && pnpm i && pnpm dev
pnpm run assets:fetch

DATABASE_URL=postgresql://chainforge:chainforge@localhost:5432/chainforge?schema=public
POLYGON_AMOY_RPC=https://polygon-amoy.g.alchemy.com/v2/<key>
PRIVATE_KEY=0x<backendSigner>
CHAIN_TOKEN_ADDRESS=0x000000000000000000000000000000000000dEaD
RELICS1155_ADDRESS=0x000000000000000000000000000000000000f011

bash scripts/deploy.sh

---

## ⚙️ 2. Deployment Script (`scripts/deploy.sh`)

```bash
#!/usr/bin/env bash
set -e
echo "🔥 Deploying ChainForge API + Worker + Web"

# Variables
APP_NAME="chainforge-v4"
PORT=8080
IMAGE="chainforge/api:latest"

# 1️⃣ Build containers
docker build -t $IMAGE -f apps/api/Dockerfile .
docker build -t chainforge/worker:latest -f apps/worker/Dockerfile .

# 2️⃣ Push or run locally
if [ "$1" == "--local" ]; then
  docker compose up -d
  echo "💠 Local forge running → http://localhost:$PORT"
else
  echo "⚙️ Deploying to Render-style platform..."
  render.yaml <<EOF
services:
  - type: web
    name: ${APP_NAME}-api
    env: docker
    plan: free
    dockerfilePath: apps/api/Dockerfile
  - type: worker
    name: ${APP_NAME}-worker
    env: docker
    dockerfilePath: apps/worker/Dockerfile
EOF
  echo "✅ Render spec generated → render.yaml"
fi

---

## ⚙️ 2. Deployment Script (`scripts/deploy.sh`)

```bash
#!/usr/bin/env bash
set -e
echo "🔥 Deploying ChainForge API + Worker + Web"

# Variables
APP_NAME="chainforge-v4"
PORT=8080
IMAGE="chainforge/api:latest"

# 1️⃣ Build containers
docker build -t $IMAGE -f apps/api/Dockerfile .
docker build -t chainforge/worker:latest -f apps/worker/Dockerfile .

# 2️⃣ Push or run locally
if [ "$1" == "--local" ]; then
  docker compose up -d
  echo "💠 Local forge running → http://localhost:$PORT"
else
  echo "⚙️ Deploying to Render-style platform..."
  render.yaml <<EOF
services:
  - type: web
    name: ${APP_NAME}-api
    env: docker
    plan: free
    dockerfilePath: apps/api/Dockerfile
  - type: worker
    name: ${APP_NAME}-worker
    env: docker
    dockerfilePath: apps/worker/Dockerfile
EOF
  echo "✅ Render spec generated → render.yaml"
fi
![CI](https://github.com/<YOUR_ORG>/<YOUR_REPO>/actions/workflows/ci.yml/badge.svg)