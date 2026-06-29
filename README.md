# Trestle DeFi Documentation

Official documentation site for Trestle DeFi, built with MkDocs Material.

**Live:** https://docs.trestle.website

## Structure

```
docs-trestle-website/
├── mkdocs.yml           # MkDocs configuration
├── docs/
│   ├── index.md         # Home page
│   ├── getting-started/ # Introduction, wallet setup, faucet
│   ├── protocol/        # Tokenomics, staking, governance
│   ├── marketplace/     # Dutch auction, escrow, AI matching
│   ├── rwa/             # RWA roadmap, standards, compliance
│   ├── tech/            # Architecture, API, contracts, audit
│   └── community/       # Security, bounty, governance
└── assets/
    ├── styles.css       # Custom styling
    ├── logo.svg         # Site logo
    └── favicon.svg      # Site favicon
```

## Development

```bash
pip install mkdocs-material
mkdocs serve    # http://localhost:8000
mkdocs build    # Build static site
mkdocs gh-deploy --force  # Deploy to GitHub Pages
```

## Deployed Contracts

### Mainnet (Polygon)
- hNOBT: `0xcF51ab7398315DbA6588Aa7fb3Df7c99D3D1F4dD`
- BroilerPlus (BRT): `0xeCb4cAc0C9e5cBd42a9Ed36467ce8f96072AD58b` (9 decimals, 5% transfer tax)
- hNobtStaking: `0xdc2b9a63CE40A64B47f484B0843FDcBEe9447b6d`
- BroilerPlusStaking: `0x214068a99c541BFD1c6267Ee69B78fAe8426F3c0`
- Distributor: `0xB2225f2e9a26688D43bC01A8Cf7aD4B179154c47`
- Gnosis Safe (Treasury): `0x64A7ef92229D2D97d1C4fd3DB15Db2d94d3D66F6`

### Testnet (Amoy)
- DigitalGoods: `0xfe50dA41BfC13e99E9276149D0b534609C39633E`
- FreelancerEscrow: `0x635Ab939A2997eFDB42AD38F6A4919d8ae45b912`

## Links
- **Website**: https://trestle.website
- **Testnet**: https://testnet.trestle.website
- **Reward Hub**: https://reward.trestle.website
- **GitHub**: https://github.com/Trestle-DeFi/trestle-docs