# Dutch Auction Logic

Trestle uses an **automated Dutch Auction** system for digital goods and freelance services. This model eliminates the need for complex order books and continuous on-chain writes.

## How It Works
The price of an item starts at a **`startingPrice`** and decreases linearly over time until it is claimed or reaches a **`floorPrice`**.

### Price Formula
```solidity
function getPrice(uint256 startTime, uint256 discountRate) public view returns (uint256) {
    uint256 timeElapsed = block.timestamp - startTime;
    uint256 priceDrop = discountRate * timeElapsed;
    uint256 currentPrice = startingPrice - priceDrop;
    
    // Ensure price doesn't drop below floor
    return currentPrice < floorPrice ? floorPrice : currentPrice;
}
```

## Vertical Markets

| Market | Description |
|--------|-------------|
| **Digital Goods** | E-books, licenses, templates: high initial price dropping to floor |
| **Freelance Services** | Milestone escrows: peak rate decreases until buyer engages |
| **Digital RWAs** | Fractional property: auction finds fair market value |

## Key Benefits

- **Gas-efficient** - Single on-chain write at listing and purchase; reads are off-chain
- **No order books** - Price discovery via time decay
- **Testnet-first** - Operations run on Polygon Amoy with faucet-funded gas

![Dutch Auction Price Decay](../images/dutch-auction.svg)
