# Optional

Welcome to Invisible Garden- ARG25.

Each participant or team will maintain this README throughout the program.  
You’ll update your progress weekly **in the same PR**, so mentors and reviewers can track your journey end-to-end.

##  Project Title

**Optional** - the options protocol

## Team

- Team/Individual Name: Derivative Technology
- GitHub Handles:
  - 0xgleb
- Devfolio Handles:
  - dGleb

## Project Description

Optional is a fully on-chain options protocol. The design prioritizes simplicity and reliability through physical settlement with 100% collateralization, eliminating the need for oracles, risk management systems, and liquidation mechanisms in the initial version. Options buyers get leverage or insurance for their positions while option sellers collect premia.

Each option series is an ERC20 token. These tokens are minted when option writers deposit collateral (underlying for calls or quote token for puts) to an ERC-4626 vault for the particular option series. Vault shares essentially represent short option, long base/quote exposure (for call/put respectively). The options are American-style, meaning they can be exercised atomically at any time prior to maturity, which allows for cash settlement via flash loans.

## Tech Stack

- Rust
- Arbitrum Stylus SDK
- OpenZeppelin Stylus contracts

## Objectives

Build a working PoC 

## Weekly Progress

### Week 1 (ends Oct 31)

**Goals:** Do preliminary research, write a spec

**Progress Summary:**  Research and spec completed


### Week 2 (ends Nov 7)

**Goals:** Option + CLOB smart contract public interface
 
**Progress Summary:** Pivoted to American over European options. Implemented the public interface


### 🗓️ Week 3 (ends Nov 14)

**Goals:** Contract implementation

**Progress Summary:**  Completely reworked the spec after trying a different protocol design


## Final Wrap-Up

Working on an earlier approach to the contract design that used ERC-1155, revealed the much better alternative design. As the result the spec has undergone very significant changes rendering the initial implementation outdated. The new spec is available in the linked repo, the updated implementation is WIP.

- **Main Repository Link:** [0xgleb/optional](https://github.com/0xgleb/optional)
- **Demo / Deployment Link (if any):**  
- **Slides / Presentation (if any):**



## 🧾 Learnings

_What did you learn or improve during ARG25?_

With the right protocol design, you can do a lot with onchain options without needing to integrate an oracle or sophisticated risk management

## Next Steps

- Implement the contracts according to the new spec
- Build an onchain CLOB (Central Limit Order Book)
- Frontend for writing, trading, and exercising options
- Automatic exercise at maturity
- Cross-series collateral management to improve capital efficiency for advanced options strategies
- Design an options market making yield product to bootstrap liquidity

_This template is part of the [ARG25 Projects Repository](https://github.com/invisible-garden/arg25-projects)._  
_Update this file weekly by committing and pushing to your fork, then raising a PR at the end of each week._
