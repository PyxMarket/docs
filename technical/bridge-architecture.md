# Bridge Architecture

The PyxMarket bridge enables USDC transfers between Arbitrum and PyxChain.

## Deposit Flow (Arbitrum → PyxChain)

1. User deposits USDC into the BridgeVault contract on Arbitrum
2. The deposit relayer monitors the vault for deposit events
3. The relayer submits a mint transaction on PyxChain
4. User receives USDC on PyxChain

## Withdrawal Flow (PyxChain → Arbitrum)

1. User burns USDC on PyxChain via the bridge precompile
2. Validators attest to the withdrawal by signing the withdrawal data
3. The withdrawal submitter collects attestations and submits to the BridgeVault on Arbitrum
4. After the dispute period (200s on testnet), the user can finalize and receive USDC on Arbitrum

## Security

- **Multi-validator attestation** — withdrawals require signatures from a quorum of validators
- **Dispute period** — a waiting period on Arbitrum before withdrawals can be finalized
- **On-chain verification** — the BridgeVault verifies validator signatures and set membership on-chain
