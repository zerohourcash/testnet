# ZHCash Testnet

This repository contains configuration and tools for launching and maintaining the **ZHCash (ZHChain) testnet**.

## 🔧 Purpose

The testnet is designed for:

- Testing new features and protocol updates without risk to the mainnet
- Debugging smart contracts and DApps before production deployment
- Experimenting with node behavior, transactions, and consensus mechanisms
- Developing and testing infrastructure (validators, API services, monitoring, etc.)

## 📂 Repository Structure

- `genesis.json` — initial chain configuration for the testnet
- `config/` — node, network, port, and block parameter settings
- `scripts/` — utilities and scripts to launch, sync, and monitor testnet nodes
- `peers.txt` — recommended peer node list for connecting to the network

## 🚀 Quick Start

```bash
git clone https://github.com/zhcash/testnet.git
cd testnet
./scripts/start-testnet.sh

See inline comments in the scripts/ directory for detailed usage and custom options.

🌐 Resources
Official Website: https://zhchain.sbs or https://zh.cash

Node Monitoring Dashboard: https://zhcash.network

ZHCash Docs: Coming soon

⚠️ Warning
The testnet is a sandbox environment and may be restarted or reset at any time. Do not use real assets or sensitive data.

ZHCash (ZHChain) — A next-generation decentralized blockchain platform.

# ZHCash Testnet

This repository contains configuration files and tools for launching and maintaining the **ZHCash (ZHChain) testnet**.

## 🔧 Purpose

The testnet is a safe environment for:

- Testing protocol updates and new features before mainnet deployment
- Developing and debugging smart contracts and applications
- Experimenting with network performance and consensus mechanisms
- Building infrastructure (validators, APIs, monitoring tools)

---

## 📂 Repository Structure

- `genesis.json` — initial chain setup for testnet
- `config/` — configuration files for nodes, ports, and network parameters
- `scripts/` — automation scripts for launching and monitoring testnet
- `peers.txt` — active peer node list for bootstrap connection

---

## 🚀 Quick Start (Manual)

```bash
git clone https://github.com/zhcash/testnet.git
cd testnet
./scripts/start-testnet.sh

tmux new -s zh-testnet
./zerohourd -testnet
# Detach: Ctrl + B, then D
# Attach again: tmux attach -t zh-testnet

tmux new -s zh-testnet
./zerohourd -testnet
# Detach: Ctrl + B, then D
# Attach again: tmux attach -t zh-testnet

docker run -d \
  --name=zh-testnet-node \
  -v $PWD/.zerohour:/root/.zerohour \
  -p 16100:16100 -p 16101:16101 \
  zhchain/zerohourd:latest \
  zerohourd -testnet

[Unit]
Description=ZHCash Testnet Node
After=network.target

[Service]
User=ubuntu
WorkingDirectory=/home/ubuntu/zhcash
ExecStart=/home/ubuntu/zhcash/zerohourd -testnet
Restart=always
RestartSec=10

[Install]
WantedBy=multi-user.target

sudo systemctl daemon-reexec
sudo systemctl enable zerohourd-testnet
sudo systemctl start zerohourd-testnet

./zerohour-cli -testnet getblockchaininfo
./zerohour-cli -testnet getpeerinfo
./zerohour-cli -testnet getwalletinfo

🌐 Resources
Official Site: https://zhchain.sbs or https://zh.cash 

Node Dashboard: https://zhcash.network

ZHCash Docs: Coming soon

⚠️ Notice
This testnet is experimental and may be restarted or reset without notice.
Do not use real assets or sensitive data.


---

Если хочешь — могу сделать и русскую версию в аналогичном стиле.

Doc by GRAViTON
