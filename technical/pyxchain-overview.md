# PyxChain Overview

PyxChain is a high-performance blockchain purpose-built for prediction markets.

## Performance

- **10,000+ TPS** — full pipeline including signature verification, mempool, consensus, and execution
- **Sub-second finality** — blocks are produced and finalized in ~200ms

## Consensus

PyxChain uses a custom BFT consensus protocol inspired by HotStuff2. Key features:

- **Double certificate finality** — blocks are finalized with notarization + finalization certificates
- **Async execution** — block execution is decoupled from consensus, allowing validators to reach agreement without waiting for execution to complete

## Execution

- **EVM-compatible** — standard Ethereum transaction format and tooling
- **Native prediction markets** — orderbook, matching engine, and redemption run as native EVM precompiles, not Solidity contracts
- **On-chain state** — all orderbook, matching, and settlement logic is fully on-chain

