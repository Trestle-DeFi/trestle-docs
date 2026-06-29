# Vault Mechanics

## The Value Capture Layer

The **Vault** is where users stake to earn Governance Tokens, the premium asset of the Trestle ecosystem.

## Vault Staking

### How It Works
1. Users stake **BroilerPlus LP tokens** (BRT/WPOL) in the Vault
2. Governance Points accumulate over time based on staking duration
3. Points convert to Governance Tokens once the Vault is live

### Vault Activation

- **Trigger**: Activated only after Marketplace Mainnet Launch and Fee Generation
- **Acquisition**: Users must stake BRT/WPOL LP to earn Governance Points
- **Supply**: Fixed at 1,000,000 tokens — No new minting

### Rewards Distribution

Governance Token rewards come from:
- **Marketplace transaction fees**
- **RWA tokenization fees**
- **Escrow fees**

### Voting Rights

Governance Token holders control:
- Platform upgrades
- Marketplace fee structures
- RWA tokenization proposals
- Treasury allocations

## Virtual Vault (Off-Chain)

### Purpose
For **hNOBT points accumulation** without gas fees.

### How It Works
- Users accumulate hNOBT points **entirely off-chain**
- Settlement produces an **EIP-712 signed voucher**
- Voucher submitted on-chain via Telegram Mini-App

### Key Features
- **No gas fees** for intermediate steps
- **Reward Hub Worker** handles point tracking
- Separate from main Vault (which handles Governance Token staking)

## Revenue Model

- **Transaction Fees**: Percentage of all marketplace transactions
- **RWA Fees**: Fees for fractionalizing assets
- **Escrow Fees**: Small fees for milestone payments

## Marketing Wallet Allocation

| Allocation | Percentage |
|------------|------------|
| LP Mining | 60% |
| Team/Future Employees | 24% |
| Community/Airdrops | 10% |
| Bug Bounty | 5% |
| Advisors | 1% |

Controlled via **Gnosis Safe** multi-sig wallet.