# Paymaster Examples Repository 📁

Welcome to the world of Paymasters!! 🎉 🌍 🎉

> ⚠️ **Work in Progress**: Please note that none of the contracts in this repository have been fully tested yet! These contracts are **not** designed for production use.

This repository contains several example Paymaster Smart Contracts that cover most common use cases. You can find the following contracts:

- 🆓 **[Gasless Paymaster](./contracts/paymaster/GaslessPaymaster.sol)**: Pays fees for any account.
- 📜 **[Allowlist Paymaster](./contracts/paymaster/AllowlistPaymaster.sol)**: Pays fees for accounts present in a predefined list (the "allow list").
- 🎫 **[ERC20 Gated Paymaster](./contracts/paymaster/ERC20gatedPaymaster.sol)**: Pays fees for accounts with a balance of a specific ERC20 token.
- 🎨 **[ERC721 Gated Paymaster](./contracts/paymaster/ERC721gatedPaymaster.sol)**: Pays fees for accounts that hold a specific ERC721 token (NFT).

Stay tuned! More Paymaster examples will be added over time. This project was scaffolded with [zksync-cli](https://github.com/matter-labs/zksync-cli).

## Repository Structure 🏗️

- `/contracts`: Contains the smart contracts.
- `/deploy`: Contains deployment and contract interaction scripts.
- `/test`: Contains test files.
- `hardhat.config.ts`: The configuration file for the Hardhat framework.

## Commands 💻

- `yarn hardhat compile`: Compiles the contracts.
- `yarn run deploy`: Executes the deployment script `/deploy/deploy-greeter.ts`. Requires [environment variable setup](#environment-variables).
- `yarn run greet`: Executes the script `/deploy/use-greeter.ts`, which interacts with the deployed Greeter contract.
- `yarn test`: Runs tests. **Make sure to check the test requirements below.**
- `yarn format`: Runs prettier formatter. 

Both `yarn run deploy` and `yarn run greet` are configured in the `package.json` file and run `yarn hardhat deploy-zksync`.

### Environment Variables 🌳

To prevent the leakage of private keys, we use the `dotenv` package to load environment variables. This is particularly used to load the wallet private key, which is required to run the deployment script.

To use it, rename `.env.example` to `.env` and input your private key.

```
WALLET_PRIVATE_KEY=123cde574ccff....
```

### Local Testing 🧪

To run tests, you'll need to start the zkSync local environment. Please refer to [this section of the docs](https://v2-docs.zksync.io/api/hardhat/testing.html#prerequisites) for details.

Without starting the zkSync local environment, the tests will fail with an error: `Error: could not detect network (event="noNetwork", code=NETWORK_ERROR, version=providers/5.7.2)`

## Have a Request? 🙋‍♀️
If you would like to see a specific type of Paymaster contract included in this repository, please let us know in the [zkync-developers/discussions](https://github.com/zkSync-Community-Hub/zkync-developers/discussions)! We value your feedback and are always open to new ideas for demonstrating different use-cases and techniques.

## Official Links 🔗

- [Website](https://zksync.io/)
- [Documentation](https://v2-docs.zksync.io/dev/)
- [GitHub](https://github.com/matter-labs)
- [Twitter](https://twitter.com/zksync)
- [Discord](https://discord.gg/nMaPGrDDwk)
