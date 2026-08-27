# base-developer-toolkit
A collection of scripts, test tools, and utility contracts optimized for Base L2 chain integration.
# Base Developer Toolkit 🛠️

A collection of lightweight utility scripts, configurations, and quickstart tools optimized for deploying and interacting with smart contracts on the Base Layer-2 network.

## 🚀 Quickstart: Network Providers & Core RPCs

```javascript
// Web3 Provider Initialization for Base Mainnet & Testnet
const { Web3 } = require('web3');

const BASE_MAINNET_RPC = "https://base.org";
const BASE_SEPOLIA_RPC = "https://base.org";

const web3 = new Web3(new Web3.providers.HttpProvider(BASE_MAINNET_RPC));

async function getBaseNetworkStats() {
    try {
        const latestBlock = await web3.eth.getBlockNumber();
        const gasPrice = await web3.eth.getGasPrice();
        console.log(`[Base Mainnet] Current Block: ${latestBlock}`);
        console.log(`[Base Mainnet] Suggested Gas Price: ${web3.utils.fromWei(gasPrice, 'gwei')} Gwei`);
    } catch (error) {
        console.error("Error connecting to Base RPC:", error);
    }
}

getBaseNetworkStats();
```

## 📜 Base Network System Constants

| Property | Base Mainnet | Base Sepolia (Testnet) |
| --- | --- | --- |
| **Chain ID** | 8453 | 84532 |
| **Currency** | ETH | ETH |
| **Block Explorer** | [Basescan](https://basescan.org) | [Sepolia Basescan](https://basescan.org) |

## 🔧 Dev Features Included
- Automated Gas Estimator for L2 transactions.
- Batch Transfer scripts for ERC-20 and ERC-721 tokens.
- Cross-chain bridge event listener templates.

---
*Maintained by the Base Ecosystem Sandbox Developers.*
