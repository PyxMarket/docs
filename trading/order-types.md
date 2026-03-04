# Order Types

PyxMarket currently supports **limit orders** on the on-chain orderbook.

## Limit Order

Place an order at a specific price. The order sits on the book until:
- It gets matched by a counterparty
- You cancel it

## Order Parameters

| Parameter | Description |
|-----------|-------------|
| Side | YES or NO |
| Price | 1-999 (probability in thousandths) |
| Amount | Number of shares |

## Cancellation

You can cancel any open order at any time. Cancellation is processed on-chain and frees your collateral immediately.
