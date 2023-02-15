<p align="center">
    <img align="center" src="/mantle.png" width="175"></img>
</p>

<h1 align="center">create-mantle-dapp</h1>

<div align="center">
    <img src="https://img.shields.io/badge/platform-mantle-black.svg?style=flat-square" alt="Platform">
    <img src="https://img.shields.io/github/license/akhileshthite/create-mantle-dapp?color=orange&style=flat-square" alt="License">
    <img src="https://img.shields.io/github/v/release/akhileshthite/create-mantle-dapp?color=blue&style=flat-square" alt="Release">
    <img src="https://img.shields.io/npm/dw/create-mantle-dapp?style=flat-square" alt="Downloads">
</div><br>

A full-stack starter template with React & Hardhat to develop, deploy, and test Solidity smart contracts on the Mantle network. The starter kit also includes pre-installed `tailwindcss`, `web3.js`, etc. packages.

## 🛠️ Installation guide

### ⌛️ create-mantle-dapp command

Open up your terminal (or command prompt) and type the following command:

```sh
npx create-mantle-dapp <your-dapp-name>

# cd into the directory
cd <your-dapp-name>
```

### 🔑 Private key

Ensure you create a `.env` file in the `root` directory. Then paste your [Metamask private key](https://metamask.zendesk.com/hc/en-us/articles/360015289632-How-to-export-an-account-s-private-key) in `.env` with the variable name `PRIVATE_KEY` as follows:

```sh
PRIVATE_KEY=1234
```

### ⚙️ Compile

Now, you can write your contracts in `./contracts/` directory, replace `Greeter.sol` with `<your-contracts>.sol` file. To write tests, go to `./test` directory and create `<your-contracts>.test.js`.

```sh
npx hardhat compile

# for testing the smart contracts
npx hardhat test
```

After successful compilation, the artifacts directory will be created in `./src/artifacts` with a JSON `/contracts/<your-contracts>.sol/<your-contracts>.json` containing ABI and Bytecode of your compiled smart contracts.

Please make the changes while [Importing]() the JSON in `./src/app.js`.

### ⛓️ Deploy

Before deploying the smart contracts, please make sure you have a `mantle testnet` in your Metamask wallet with sufficient funds, follow this [quickstart](https://docs.mantle.xyz/introducing-mantle/quick-start) guide if you do not have one.

Also, make changes in `./scripts/deploy.js` (replace the greeter contract name with `<your-contract-name>`).

For deploying the smart contracts to Mantle network, type the following command:

```sh
npx hardhat run --network mantle_testnet scripts/deploy.js
```

Copy-paste the deployed contract address [here]()

```sh
<your-contract> deployed to: 0x...
```

### 💻 React client

start react app

```sh
npm start
# Starting the development server...
```

Please read the [hardhat documentation](https://hardhat.org/hardhat-runner/docs/getting-started#quick-start) and [mantle documentation](https://www.mantle.xyz/developers) for more details.

## ⚖️ License

create-mantle-dapp is licensed under the [MIT License](https://github.com/akhileshthite/create-mantle-dapp/blob/main/LICENSE).

<hr>
Don't forget to leave a star ⭐️ ~ <a href="https://twitter.com/akhileshthite_" target="_blank"><img src="https://img.shields.io/twitter/follow/akhileshthite_?style=social" alt="twitter" /></a>
