# Audit & Security Status

## Current Audit Phase

**Status:** Testnet (Amoy) Beta  
**Approach:** Community-Driven Audit & Bug Bounties

## Security Audits

| Component | Status | Notes |
|-----------|--------|-------|
| Core Contracts | ✅ Verified | Mainnet & Testnet verified on Polygonscan |
| Internal Review | ✅ Completed | All fixes applied |
| Formal Audit | 🚧 Scheduled | Q3 2026 for Marketplace contracts |

## Bug Bounty Program (Testnet Phase)

### Rewards

| Severity | Reward |
|----------|--------|
| Critical | Governance Points + "Security Scout" status (priority Governance Token allocation) |
| High | Governance Points + Security Scout status |
| Medium | hNOBT points via Telegram Reward Hub |

### Reporting

Report vulnerabilities via:
- **GitHub Issues** (Private)
- **Discord Security Channel**

### Future

Upon Mainnet launch with TVL, transitions to **cash-based bounty** (Immunefi or similar).

## Best Practices

1. **Never share** your private keys
2. **Verify contract addresses** on Polygonscan before interacting
3. Use a **dedicated wallet** for DeFi interactions
4. Always **test on testnet first**

## Hall of Fame

Top contributors listed permanently in the Security Contributors section upon Mainnet launch.

## Audit Checklist

- [x] Reentrancy protection on all staking contracts
- [x] Access control (Ownable) implemented
- [x] Emergency withdrawal removed
- [x] ERC20 recovery properly guarded
- [x] Rate caps added for emissions
- [x] Referral percentage configurable with bounds

---

*Last updated: June 2026*