# Testnet Smart Contracts (Amoy)

The Marketplace and Escrow logic are currently live on the **Amoy Testnet**.

## Contract Addresses (as of 2026-06-29)

| Contract | Address | Purpose | Status |
| :--- | :--- | :--- | :--- |
| MockGovernanceToken (xGOV) | `0x686C4711a35633479F3Fed0D83b34DA63878CA00` | Governance token | ✅ Verified |
| FeeDistributor | `0xbA3B12F5633da2794c97CF330B19E510e2BbB05` | Fee distribution | ✅ Verified |
| DigitalGoods | `0xfe50dA41BfC13e99E9276149D0b534609C39633E` | Dutch Auction & Escrow | ✅ Verified |
| FreelancerEscrow | `0x635Ab939A2997eFDB42AD38F6A4919d8ae45b912` | Milestone payments | ✅ Verified |
| DigitalRWA | `0x18dF08d96F303c6149a7f8CC4800BCa7fcAEB0Fd` | RWA tokenization | ✅ Verified |
| UserProfile | `0x4cEaa30839E3E463484c2D66900fdD6484022054` | Reviews & profiles | ✅ Verified |
| Mock USDC | `0x6A08C1eE8102B41935a758b5E3093b075113E615` | Test stablecoin | ❌ Not verified |
| Mock USDT | `0xdd89E04e5bB9B79775A87Fa9666C5Fe03a01e169` | Test stablecoin | ❌ Not verified |

## Testnet Faucet

Need MATIC for testing?
- [Amoy Faucet](https://faucet.polygon.technology/)

## Live Demo

- [Testnet Marketplace](https://testnet.trestle.website)

## Recent Fixes (2026-06-29)

| Issue | Contract | Status |
|-------|----------|--------|
| M-1 | `FreelancerEscrow.fundProject()` | ✅ Fixed - prevents over-funding |
| M-2 | `FreelancerEscrow.approveMilestone()` | ✅ Fixed - requires `InProgress` status |
| M-3 | `FreelancerEscrow.autoApproveMilestone()` | ✅ Fixed - added completion check |
| M-5 | `DigitalRWA.mint()` whitelist | ✅ Fixed - admin cannot mint to non-whitelisted |
| M-6 | `FeeDistributor.setSplitBps` | ✅ Fixed - allows 100% split |
| M-7 | `FreelancerEscrow.fundProjectWithToken()` | ✅ Fixed - same `=` not `+=` fix |
