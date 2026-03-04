# On-Chain Orderbook

PyxMarket uses a fully on-chain central limit order book (CLOB). Every order placement, cancellation, match, and settlement is executed on-chain.

## How It Works

1. A trader submits a limit order (side, price, amount) as an EVM transaction
2. The prediction precompile (`0x105`) processes the order
3. If a matching counterparty exists, the trade executes immediately
4. If no match, the order sits on the book until filled or cancelled
5. All state changes emit EVM logs for real-time tracking

## Why On-Chain

Most prediction markets use off-chain orderbooks with on-chain settlement. PyxMarket puts everything on-chain:

- **Transparent** — anyone can verify order flow and matching
- **No front-running** — deterministic execution order within blocks
- **No centralized sequencer** — the orderbook is part of the consensus state
- **Composable** — other smart contracts can interact with the orderbook

## Performance

The orderbook runs as an EVM precompile (native Rust code) rather than a Solidity smart contract. This gives near-native execution speed while maintaining EVM compatibility for tooling and events.
