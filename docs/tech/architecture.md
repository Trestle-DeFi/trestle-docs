# Technical Architecture

Trestle uses a **Serverless Microservices Architecture** powered by **Cloudflare Workers** for speed and cost-efficiency.

## Core Components
| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **Reward Hub** | `Hono.js` on Workers | Tasks API, user management, claim issuance |
| **Virtual Vault** | `Hono.js` on Workers | Off-chain staking, yield accrual, EIP-712 vouchers |
| **Moderation** | `Hono.js` on Workers | Spam detection, AI chat, auto-mute |
| **Database** | **D1** (SQLite) | Shared user data, job history |
| **Cache** | **KV Store** | Job lifecycle, AI config |
| **Queue** | **Cloudflare Queues** | Async AI processing (no timeouts) |
| **AI** | **Workers AI** + OpenAPI | Dispute analysis, matching, fraud detection |

## Off-Chain vs. On-Chain
- **Off-Chain:** User tasks, AI processing, voting simulation, spam filtering.
- **On-Chain:** Fund settlement, staking, token transfers, final dispute resolution.
- **Bridge:** **EIP-712 Signed Vouchers** allow users to claim rewards on-chain without gas fees for the intermediate steps.
