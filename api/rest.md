# REST API

Base URL: `https://api.pyxmarket.com/api/v1`

## Endpoints

### Events

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/events` | List all events |
| GET | `/events/{event_id}` | Get event details |
| GET | `/events/{event_id}/markets` | Get markets with BBO prices |
| GET | `/events/{event_id}/orderbook` | Get full orderbook |
| GET | `/events/{event_id}/fills` | Get recent fills |

### Orders

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/orders` | List orders (query: `address`, `market_id`) |

### Fills

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/fills` | List recent fills |

### Accounts

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/balances/{address}` | Get account balances |
| GET | `/positions/{trader}` | Get trader positions |

### Faucet

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/faucet` | Request testnet tokens (body: `{"address": "0x..."}`) |

## Example

```bash
# Get all events
curl https://api.pyxmarket.com/api/v1/events

# Get orderbook for event 1
curl https://api.pyxmarket.com/api/v1/events/1/orderbook

# Get balances
curl https://api.pyxmarket.com/api/v1/balances/0xYourAddress
```
