# Markets

PyxMarket hosts prediction markets on real-world events.

## Market Structure

Each **event** contains one or more **markets** (outcomes to trade). For example:

- **Event**: "2024 US Presidential Election"
  - Market 1: "Will Trump win?" (YES/NO)
  - Market 2: "Will Biden win?" (YES/NO)

## Prices

Prices range from **$0.000 to $1.000** with 3 decimal places of precision. A price reflects the market's implied probability.

| Price | Implied Probability | Meaning |
|-------|-------------------|---------|
| $0.100 | 10% | Market thinks event is unlikely |
| $0.500 | 50% | Coin flip — market is uncertain |
| $0.700 | 70% | Market thinks event is likely |
| $0.950 | 95% | Market is very confident |

- YES + NO prices sum to approximately $1.000
- If YES is trading at $0.700, NO is trading at ~$0.300
- Buy YES at $0.700, if the event happens you receive $1.000 (profit: $0.300)

## Auto Redemption

If you hold both YES and NO shares in the same market, they are automatically redeemed for $1.000 per pair. This happens instantly — no transaction needed. For example, if you hold 10 YES and 3 NO, 3 pairs are redeemed for $3.000 USDC and you keep 7 YES shares.

## Resolution

Markets resolve when the real-world event outcome is determined. Winning shares pay $1.000, losing shares pay $0.000. Payouts are distributed automatically to your wallet — no claiming transaction needed.
