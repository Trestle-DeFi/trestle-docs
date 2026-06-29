# API Endpoints

## Backend Workers Architecture

Trestle Platform uses **Cloudflare Workers** with a serverless microservices architecture:

| Worker | URL | Purpose | Status |
|--------|-----|---------|--------|
| **trestle-reward** | `reward-api.trestle.website` | Tasks, claims, users, config, AI endpoints | ✅ Live |
| **trestle-vault** | `vault.trestle.website` | Virtual vault staking, yield accrual, EIP-712 vouchers | ✅ Live |
| **trestle-moderation** | `moderation.trestle.website` | Telegram/Discord webhooks, spam shield, AI chat | ✅ Live |

## Frontend URLs

| Component | URL | Status |
|-----------|-----|--------|
| Reward Hub | https://reward.trestle.website | ✅ Live (Mainnet) |
| Telegram Mini-App | https://t.me/trestlehub_bot/app | ✅ Live |
| Testnet Marketplace | https://testnet.trestle.website | ✅ Live (Amoy) |
| Mainnet Marketplace | https://trestle.website | 🚧 Coming Soon |

## AI & Queue System

- **AI Queue**: Cloudflare Queue `trestle-ai-queue` for async AI request processing
- **Job Lifecycle**: KV-backed (`job:uuid`) with 24h TTL
- **Status Flow**: `pending` → `processing` → `done`/`error`
- **Providers**: Cloudflare Workers AI (primary) with fallback pool (OpenAI-compatible APIs)
- **Moderation**: HuggingFace DistilBERT toxicity classifier + regex spam patterns

## Database & Storage

| Component | Technology | Purpose |
|-----------|------------|---------|
| Database | D1 (SQLite) | Shared database for all workers |
| Cache | KV Store | Job lifecycle, AI provider config |
| Queue | Cloudflare Queues | Async AI processing |

## Smart Contract Addresses

### Mainnet (Polygon)

| Contract | Address | Purpose |
|----------|---------|---------|
| hNOBT | `0xcF51ab7398315DbA6588Aa7fb3Df7c99D3D1F4dD` | Community growth token |
| BroilerPlus | `0xeCb4cAc0C9e5cBd42a9Ed36467ce8f96072AD58b` | Liquidity anchor token (9 decimals, 5% transfer tax) |
| Distributor | `0xB2225f2e9a26688D43bC01A8Cf7aD4B179154c47` | Claimable airdrop |
| hNobtStaking | `0xdc2b9a63CE40A64B47f484B0843FDcBEe9447b6d` | hNOBT staking |
| BroilerPlusStaking | `0x214068a99c541BFD1c6267Ee69B78fAe8426F3c0` | BroilerPlus staking |
| Gnosis Safe | `0x64A7ef92229D2D97d1C4fd3DB15Db2d94d3D66F6` | Multi-sig wallet |

### Testnet (Amoy)

| Contract | Address | Purpose |
|----------|---------|---------|
| DigitalGoods | `0xfe50dA41BfC13e99E9276149D0b534609C39633E` | Dutch Auction & Escrow |
| FreelancerEscrow | `0x635Ab939A2997eFDB42AD38F6A4919d8ae45b912` | Milestone payments |

## API Rate Limits

- **Public endpoints**: 100 requests/minute
- **Authenticated endpoints**: 1,000 requests/minute
- **AI endpoints**: Batched via Queue (no direct rate limit)