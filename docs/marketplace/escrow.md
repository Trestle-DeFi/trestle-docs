# Escrow & Dispute Resolution

Trust is enforced by **Smart Contract Escrow** and a **Decentralized Dispute Resolution** layer.

## Smart Contract Escrow
1. **Funding:** Buyer deposits funds into the `EscrowContract`.
2. **Milestones:** Funds are released in stages as work is verified.
3. **Completion:** Final release triggers only after buyer approval or dispute resolution.

## Decentralized Dispute Resolution
If a buyer and freelancer disagree, the dispute is escalated to a **Community Jury**.

### Resolution Layers
1. **AI-Assisted Analysis:** Open-source AI models (LLaVA, Llama 3) analyze evidence (chat logs, code diffs, deliverables) and recommend a ruling.
2. **Kleros Integration:** If AI is inconclusive, the case is sent to **Kleros** for human jury arbitration.
3. **Community Jurors:** Trestle token holders can become jurors, earning `hNOBT` and `Governance Points` for resolving cases.

## AI Fraud Detection
Real-time monitoring using **Cloudflare Workers** and **HuggingFace** classifiers detects:
- **Sybil Attacks:** Fake accounts creating fake jobs.
- **Spam Patterns:** Automated bot messages.
- **Toxicity:** Harassment in chat threads.

*Violations result in automatic 24-hour mutes or permanent bans, enforced via the `ModerationWorker`.*

![Escrow Flow Diagram](../images/escrow-flow.svg)
