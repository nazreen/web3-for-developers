## LayerZero v2 tutorial

Official Getting Started: https://docs.layerzero.network/contracts/getting-started

## Prepare

Add Ethereum Sepolia: https://revoke.cash/learn/wallets/add-network/ethereum-sepolia

Add Optimism Sepolia: https://revoke.cash/learn/wallets/add-network/optimism-sepolia


Get Sepolia ETH (in-browser mining): https://sepolia-faucet.pk910.de/

OR https://www.alchemy.com/faucets/ethereum-sepolia (slow)

OR https://faucetlink.to/sepolia

Get Optimism ETH (Github, 0.05 ETH): https://app.optimism.io/faucet


## Zero Padding

To convert an EVM address from 20 bytes to 32 bytes, we need to understand the relationship between a hex number and bytes.

Remember that 1 byte = 8 bits and that a hex number can 16 possible values (from 0 till F)

16 in binary form would take up 4 binary digits, or in other words, 4 bits. That's half a byte.

So each hex character represents half a byte.

So, adding 12 bytes would require 12 bytes / 0.5 byte per hex character = 24 hex characters.

below are 24 0's. Yes, I counted them for you!

000000000000000000000000 

## Endpoint IDs

* Ethereum Sepolia: 40161
* Optimism Sepolia: 40232

## Endpoint address

The docs at https://docs.layerzero.network/contracts/getting-started wrongly quotes the endpoint addresses for both chain as 0x464570adA09869d8741132183721B4f0769a0287

it should be 0x6edce65403992e310a62460808c4b910d972f10f

You can view the latest addresses at https://docs.layerzero.network/contracts/endpoint-addresses

## Explorer

https://testnet.layerzeroscan.com/
