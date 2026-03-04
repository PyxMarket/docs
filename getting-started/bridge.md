# Bridge

The bridge moves USDC between Arbitrum and PyxChain.

## Deposit (Arbitrum → PyxChain)

1. Click **Deposit** in the header
2. Enter the USDC amount
3. Approve the transaction (your wallet will switch to Arbitrum automatically)
4. Wait for the deposit to be relayed to PyxChain
5. Your PyxChain USDC balance updates automatically

## Withdraw (PyxChain → Arbitrum)

1. Click **Withdraw** in the header
2. Enter the USDC amount
3. Confirm the burn transaction on PyxChain
4. Validators attest to the withdrawal and submit it to Arbitrum
5. After a 200-second dispute period, the withdrawal is finalized
6. USDC arrives in your Arbitrum wallet

## Dispute Period

Withdrawals have a 200-second dispute period on Arbitrum for security. During this time, validators can challenge fraudulent withdrawals. 
