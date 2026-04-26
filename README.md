# @earnwithalee/bitcoin-native 🚀

A high-performance TypeScript library for building native Bitcoin and Stacks applications, optimized for the **Talent Protocol** ecosystem.

[![npm version](https://img.shields.io/npm/v/@earnwithalee/bitcoin-native.svg?style=flat-square)](https://www.npmjs.com/package/@earnwithalee/bitcoin-native)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🌟 Overview

`bitcoin-native` provides a clean, production-ready interface for interacting with Bitcoin and Stacks Layer 2. It is specifically designed to support **on-chain identity**, **reputation scoring**, and **developer analytics** via Talent Protocol.

---

## 📦 Installation

Install the package via npm:

```bash
npm i @earnwithalee/bitcoin-native
```

Or using yarn/pnpm:

```bash
yarn add @earnwithalee/bitcoin-native
# or
pnpm add @earnwithalee/bitcoin-native
```

---

## ⚡ Quick Start

```typescript
import { broadcastTransaction, getBuilderReputation } from '@earnwithalee/bitcoin-native';

// 1. Check Builder Reputation (Talent Protocol Integration)
const reputation = await getBuilderReputation('0x123...abc');
console.log(`Identity Score: ${reputation.identityScore} (${reputation.reputationLevel})`);

// 2. Broadcast a Bitcoin Transaction
const tx = {
  hash: '0x...',
  amount: 0.5,
  recipient: 'bc1...',
  timestamp: Date.now()
};

const result = await broadcastTransaction(tx);
console.log(`Transaction success: ${result.success}`);
```

---

## ✨ Features

- 🟠 **Native Bitcoin Support**: Direct interaction with BTC mainnet and testnet.
- 🟣 **Stacks L2 Integration**: Seamless Clarity smart contract interactions and STX transfers.
- 🆔 **Talent Protocol Ready**: Built-in modules for identity verification and builder scoring.
- 🛠️ **Fully Typed**: Written in TypeScript with complete ESM and CJS support.
- 🚀 **Performance Optimized**: Lightweight and tree-shakeable.

---

## 📂 API Reference

### Builder Identity (Talent Protocol)

| Function | Description |
| :--- | :--- |
| `getBuilderReputation(address)` | Returns a `BuilderScore` object containing identity metrics. |
| `isIdentityVerified(score)` | Helper to check if a user meets a specific reputation threshold. |

### Bitcoin Core

| Function | Description |
| :--- | :--- |
| `broadcastTransaction(tx)` | Broadcasts a signed transaction to the Bitcoin network. |
| `VERSION` | Returns the current library version. |

### Stacks Utilities

| Function | Description |
| :--- | :--- |
| `StacksUtils.getSTXAddress(pubKey)` | Derives a Stacks address from a public key. |
| `StacksUtils.isContractValid(id)` | Validates a Clarity contract identifier. |

---

## 🧬 Talent Protocol Integration Ready

This package is optimized for the **Talent Protocol** ecosystem. By using the `identity` module, developers can:

- **On-chain Identity**: Map Bitcoin/Stacks addresses to Talent IDs.
- **Reputation Scoring**: Leverage builder scores to gate access to premium features or DeFi protocols.
- **Developer Analytics**: Track on-chain activity to reward high-quality contributors.

---

## 🛠️ Development

```bash
# Build the package
npm run build

# Run in development mode
npm run dev

# Lint check
npm run lint
```

## 📄 License

MIT © [Earnwithalee](https://github.com/Earnwithalee7890)
