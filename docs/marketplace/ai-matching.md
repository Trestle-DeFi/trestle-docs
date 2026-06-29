# AI Integration & Matching

Trestle leverages **Decentralized AI** to optimize the marketplace without a central authority.

## AI Node Operators
Community members can run **AI Nodes** to provide compute power.
- **Models:** Llama 3, Mixtral, StableLM, LLaVA.
- **Rewards:** Operators earn `hNOBT` for successful inference jobs.
- **Governance:** Node operators participate in AI model updates and reputation scoring.

## Use Cases
### 1. Freelancer Matching
- **Skill Matching:** AI analyzes freelancer profiles and job descriptions to suggest the best matches.
- **Reputation Scoring:** AI aggregates on-chain history and off-chain reviews to generate a dynamic "Trust Score."

### 2. Dispute Resolution
- **Evidence Analysis:** AI reads chat logs and code commits to recommend fair outcomes.
- **Speed:** Reduces resolution time from days to minutes for simple cases.

### 3. RWA Verification
- **Document Analysis:** AI (LLaVA) scans property deeds and legal documents for RWA tokenization.
- **Compliance:** Checks against regulatory databases (Chainlink Oracles).

## Technical Architecture
- **Queue System:** `Cloudflare Queues` handle async AI requests.
- **Job Lifecycle:** Tracked in `KV Store` (Pending → Processing → Done/Error).
- **Timeouts:** No endpoint timeouts; instant user feedback via async polling.

![AI Integration Architecture](../images/ai-architecture.svg)
