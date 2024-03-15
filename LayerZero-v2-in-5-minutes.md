Simplifying things
- The scaffolded project will have by default 3 chains: Ethereum Sepolia, Avalanche Fuji and Polygon Mumbai
- We only need 2 chains, to demonstrate how LayerZero works, so we'll remove one. At the moment, Ethereum Sepolia test ether is annoying to get, so we'll remove Ethereum Sepolia.

# Prepare
- comment out the `sepolia` entry in `hardhat.config.ts` (if you don't, when deploying, the lz cli will list fuji as an option)
- comment out lines in `layerzero.config.ts` under contracts and connections that related to Ethereum Sepolia
- add the networks involved in the scaffolded project (Avalanche Fuji, Polygon Mumbai)
  - you can use https://chainlist.org/ to add the networks (ensure you check the 'include testnets' checkbox) 
- get testnet gas tokens
  - Avalanche Fuji: https://core.app/tools/testnet-faucet/
  - Polygon Mumbai: https://faucet.polygon.technology/ (requires a Discord connection and joining the Polygon discord) OR https://www.alchemy.com/faucets/polygon-mumbai (requires an Alchemy account, which I recommend)

# Wiring
Current, the docs tell you to run `npx hardhat lz:oapp:wire`, which is incomplete. You should run instead: `npx hardhat lz:oapp:wire --oapp-config layerzero.config.ts`

# Manual Test

## Endpoints IDs

- Avalanche Fuji: 40106

- Polygon Mumbai: 40109

## Zero padding

000000000000000000000000

## Options Generator
Remix: https://remix.ethereum.org/#url=https://docs.layerzero.network/LayerZero/contracts/OptionsGenerator.sol&lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.24+commit.e11b9ed9.js


Appendix
On Wiring and Configurations: https://docs.layerzero.network/contracts/wiring
Verifying contract: https://sourcify.dev/
