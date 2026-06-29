# Tokenomics

The Trestle ecosystem utilizes a **three-token system** designed to create a self-sustaining economic flywheel.

## The Three-Token System

| Token | Symbol | Purpose | Supply Model |
| :--- | :--- | :--- | :--- |
| **Community Growth** | `hNOBT` | Tasks, Referrals, Profile Boosts | **Dynamic** (No Max Supply) |
| **Liquidity Anchor** | `BroilerPlus` (BRT) | LP Mining, Staking Rewards | **Fixed** (1 Quadrillion, 9 decimals) |
| **Value Capture** | `Governance` | Fee Sharing, Voting | **Fixed** (1,000,000) |

## BroilerPlus (BRT) Emission Model

**Total Supply:** 1 Quadrillion (1,000,000,000,000,000)

### Mining Allocation
**60%+** of the total supply is reserved exclusively for **Liquidity Mining & Staking Rewards**.

### Dynamic Emissions
Unlike static protocols, Trestle uses a **Governance-Driven Emission Model**:
- **Rate Adjustment:** The reward rate per block is adjustable by **Governance Token Holders** via on-chain voting.
- **Market Response:**
  - *Bear Market:* Governance can lower emissions to conserve the pool.
  - *Bull Market:* Governance can increase emissions to bootstrap deep liquidity.
- **Sustainability:** This ensures the mining pool lasts for **10+ years** rather than being exhausted in months.

### Distribution Breakdown
- **60%+**: LP Mining & Staking Rewards (Dynamic Emissions)
- **25%**: Initial Liquidity Providers (Market Making)
- **15%**: Treasury & Ecosystem Growth (Governance Controlled)

> **Note:** The Mining Pool is locked in the `Mine` contract. Once exhausted, emissions stop until new allocations are approved by Governance.

> **BRT Transfer Tax:** BRT has a **5% transfer tax** enforced at the token-contract level. Staking contracts gross up rewards to account for this tax, ensuring users receive the full intended amount.

![Trestle DeFi Flywheel](../images/flywheel.svg)
![Tokenomics Distribution](../images/tokenomics.svg)
