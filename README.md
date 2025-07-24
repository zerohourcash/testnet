# testnet
# ZHCash Testnet

This repository is designed to deploy and maintain the **testnet** of the **ZHCash (ZHChain)** blockchain.

## 🔧 Purpose

Testnet is used for:

- Testing new features and network updates without risking the mainnet
- Debugging smart contracts and applications before launching them in production
- Conducting experiments and analyzing node behavior
- Developing and testing infrastructure (validators, nodes, API, etc.)

## 📂 Repository contents

- `genesis.json` — testnet chain initialization file
- `config/` — node, port, block and network settings
- `scripts/` — utilities and scripts for launching, synchronizing and diagnosing testnet nodes
- `peers.txt` — list of recommended peer nodes for connection

## 🚀 Quick start

```bash
git clone https://github.com/zhcash/testnet.git
cd testnet
./scripts/start-testnet.sh
