# WebSocket API

PyxMarket provides real-time updates via WebSocket connections.

## Chain WebSocket

Endpoint: `wss://ws.pyxmarket.com`

Subscribe to on-chain events including fills, order placements, and cancellations using standard Ethereum log subscriptions.

### Subscribe to Logs

```json
{
  "jsonrpc": "2.0",
  "method": "eth_subscribe",
  "params": ["logs", {"topics": ["<event_selector>"]}],
  "id": 1
}
```

### Event Selectors

| Event | Selector |
|-------|----------|
| Fill | `0x2a5f673289bff230b4b8084f7c4488afc603f6ea4c36ce2069fb2cadbffb0b66` |
| OrderPlaced | `0x8b63a49b449dabf45be74296b539684218c871f0ab2f405c3f79d87a5c6dc0d9` |
| OrderCancelled | `0x8c5750fdef1947bcda93ba62de2f1adb8c5a8c5c1b6cdb9cc253e55516b99f8e` |
| OrderModified | `0x8a3361c421d0a0aa0d37db4c247d4e358d12d66e40cfbdbcfd7cc8ffe4372e6e` |

## Trade API WebSocket

Endpoint: `wss://api.pyxmarket.com/ws/trade`

Higher-level WebSocket for trade management. Provides parsed order and fill events.
