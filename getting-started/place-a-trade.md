# Place a Trade

## Steps

1. Browse markets on the [Markets](https://pyxmarket.com/markets) page
2. Click on a market to open the trading view
3. Choose **YES** or **NO**
4. Set your price (0.0 to 99.9, representing probability in %) and amount
5. Click **Place Order**
6. Your order appears on the orderbook and will be matched when a counterparty trades

## Example

If you think "Bitcoin above $100k by Friday" is 70% likely:
- Buy **YES** at price 700 (70 cents)
- If the event resolves YES, you receive $1.00 per share (profit: $0.30)
- If the event resolves NO, you lose your $0.70

## Order Matching

Orders are matched on a fully on-chain orderbook. When your bid meets an existing ask (or vice versa), the trade executes immediately on-chain. Unmatched orders stay on the book until filled or cancelled.
