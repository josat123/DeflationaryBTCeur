# DBTCEUR - Whitepaper (Executive Summary)

## Abstract
DBTCEUR is a native deflationary token on Polygon that combines reward mechanisms for liquidity providers and long holders with a scheduled burn governed by the DAO. The goal is to create a euro-denominated, deflationary reserve currency, interoperable with DBTC, and managed by the DAO.

## Key Concepts
- **Initial Supply**: 700,000,000 DBTCED
- **Stable Target**: 500,000,000 DBTCED
- **Min Supply**: 250,000,000 DBTCED
- **Mechanics**: Transfer fee (2%), split: 60% LP rewards, 30% long holders, 10% burn.

## Mechanics
1. **Fee and Collection**: Each transfer (not exempted) sends the fee to the contract. Fees are periodically distributed, calculated, and assigned (pendingRewards) to LPs, longs, and stakes.
2. Scheduled Burn: The contract burns only-from-contract balance at a defined interval (e.g., every 30 days) until it reaches MIN_SUPPLY.
3. DAO Governance: The DAO can vote to change parameters (rate, treasury spending, airdrops). Critical ownership is managed with Ownable2Step, and the immutable wallet ownerFee is set in the constructor.

## Security & Audits
- OpenZeppelin used for ERC20, Pausable, ReentrancyGuard, Ownable2Step.
- All external token transfers use IERC20 checks.
- Non-Reentrant on state-changing public functions.
- Recommended: Paid professional audit before mainnet listing.

## Roadmap
- Phase 1: Deploy core contracts, create liquidity pools (Uniswap/QuickSwap/Sushi)
- Phase 2: DAO activation and first burn cycle after initial liquidity
- Phase 3: Listings, audit, marketing

## Token Use Cases
- Medium of exchange within ecosystem
- Collateral for DAO vaults
- Liquidity incentives