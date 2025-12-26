<p align="center">
  <img src="dbtceur_logo.png" alt="DBTCEUR Logo" width="150"/>
</p>

<h1 align="center">DBTCEUR - DeflationaryDBTCEUR Protocol</h1>
<p align="center">
  Next-Generation Deflationary Token & Ecosystem on Polygon
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Foundry-Tests%20Passed-brightgreen" alt="Foundry Tests"/>
  <img src="https://img.shields.io/badge/Security-Audit%20Passed-success" alt="Security Audit"/>
  <img src="https://img.shields.io/badge/MIT%20License-blue" alt="MIT License"/>
  <img src="https://img.shields.io/badge/Polygon%20Network-purple" alt="Polygon Network"/>
  <img src="https://img.shields.io/badge/Solidity-0.8.20-lightgrey" alt="Solidity 0.8.20"/>
  <img src="https://img.shields.io/badge/Contract-Verified-brightgreen" alt="Contract Verified"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-blue" alt="Version"/>
</p>

---

## 📋 Contract Overview
**Contract Name:** DeflationaryDBTC€ur  
**Symbol:** DBTCED  
**Network:** Polygon Mainnet  
**Contract Address:** [`0x32466616c9fca520cccc2e7b057cf99e9a4136cd`](https://polygonscan.com/address/0x32466616c9fca520cccc2e7b057cf99e9a4136cd)

## Quick Links
- Website: https://deflationarybtceur.online
- Contract (Polygon): [Polygonscan](https://polygonscan.com/address/0x32466616c9fca520cccc2e7b057cf99e9a4136cd#code)

## 🚀 Features

### 🔥 Deflationary Mechanism
- **Initial Supply:** 700,000,000 DBTCED
- **Target Supply:** 500,000,000 DBTCED  
- **Minimum Supply:** 250,000,000 DBTCED
- **Scheduled Burns** with configurable intervals
- **Manual & DAO-controlled burn functions**

### 💰 Fee Structure
- **Transfer Fee:** 0.2% on all transfers
- **Fee Distribution:**
  - 0.02% to owner wallet
  - 0.18% to treasury
- **Fee Exclusions** for owner, treasury, DAO, and contract

### 🛡️ Security Features
- **Reentrancy Guard** protection
- **Pausable** contract functionality
- **Ownable with Two-Step Transfer**
- **Comprehensive Access Controls**

## 📊 Tokenomics
Supply Structure:
- Initial Supply: 700,000,000 DBTCED
- Target Supply: 500,000,000 DBTCED
- Minimum Supply: 250,000,000 DBTCED
- Current Supply: {700_000_000 - 0} DBTCED

Fee Mechanism:
- Transfer Tax: 0.2%
- Owner Share: 0.02%
- Treasury Share: 0.18%

## 🏗️ Project Structure
DBTCED-Token/
- script/ # Deployment scripts
- src/ # Contract source code
  - DBTCEURDeflationary.sol
- test/ # Foundry test files
  - DBTCEURTest.t.sol
- .github/ # CI/CD workflows
- README.md # This file
- foundry.toml # Foundry configuration

## 🧪 Testing with Foundry

### Prerequisites
```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup

Run Tests
```bash

forge coverage

📜 Contract Functions

Core Functions

    transfer() - With built-in fee mechanism

    manualBurn(amount) - Owner-controlled burns

    daoBurn(amount) - DAO-controlled burns

    addLiquidity() - Liquidity pool management

Configuration Functions

    setOwnerWallet(address)

    setTreasury(address)

    setDAO(address)

    setRouter(address)

Security Functions

    pause() / unpause() - Emergency controls

    Ownership transfer with two-step verification

🔧 Deployment

Compile Contract
```bash
forge build

Deploy to Network
```bash
forge create --rpc-url <RPC_URL> \
  --private-key <PRIVATE_KEY> \
  src/DBTCEURDeflationary.sol:DBTCEURDeflationary \
  --constructor-args 2592000  # 30-day burn interval

Verify Contract
```bash
forge verify-contract \
  --chain polygon \
  0x32466616c9fca520cccc2e7b057cf99e9a4136cd \
  src/DBTCEURDeflationary.sol:DBTCEURDeflationary \
  --constructor-args 2592000

📈 Burn Schedule

Automated burning with configurable intervals

Supply target mechanism

DAO governance for burns

Emergency manual burn capability

🎯 Roadmap

Contract Development & Testing

Foundry Test Suite Implementation

Security Audit Completion

Mainnet Deployment

Liquidity Pool Establishment

DAO Governance Launch

Ecosystem Expansion

👥 Team & Governance

Contract Owner: Initial administration rights

DAO: Community governance implementation

Treasury: Ecosystem fund management

📄 License

MIT License – see contract header for details.

🛣️ Support

Documentation: Project Wiki

Issues: GitHub Issues

Discussions: Community Forum
yaml


