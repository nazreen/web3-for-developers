Simplifying things
- The scaffolded project will have by default 3 chains: Ethereum Sepolia, Avalanche Fuji and Polygon Mumbai
- Testnet gas tokens for Avalanche Fuji is very annoying to get. The official faucet and Quicknode's both required you to connect using an address that has a balance on mainnet. Bitbond's require you to complete a profile. As such, we will exclude it. LayerZero probably included 3 to demonstrate how easy it is to deploy using the CLI, but we only really need 2. We'll keep Ethereum Sepolia and Polygon Mumbai since it's fairly easy to get testnet gas tokens on them both.

# Prepare
- comment out the `fuji` entry in `hardhat.config.ts` (if you don't, when deploying, the lz cli will list fuji as an option)
- comment out lines in `layerzero.config.ts` under contracts and connections that related to Avalanche Fuji
- add the networks involved in the scaffolded project (Ethereum Sepolia, Polygon Mumbai)
  - you can use https://chainlist.org/ to add the networks (ensure you check the 'include testnets' checkbox) 
- get testnet gas tokens
  - Ethereum Sepolia: https://sepolia-faucet.pk910.de/
  - Polygon Mumbai: https://faucet.polygon.technology/ (requires a Discord connection and joining the Polygon discord) OR https://www.alchemy.com/faucets/polygon-mumbai (requires an Alchemy account, which I recommend)

# Wiring
Current, the docs tell you to run `npx hardhat lz:oapp:wire`, which is incomplete. You should run instead: `npx hardhat lz:oapp:wire --oapp-config layerzero.config.ts`

Appendix
On Wiring and Configurations: https://docs.layerzero.network/contracts/wiring
