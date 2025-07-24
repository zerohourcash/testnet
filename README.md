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

Вот профессиональный перевод статьи на **английский язык** — для публикации на сайте, в документации или блоге ZHCash (ZHChain):

---

# 📡 The Role of the Testnet in the ZHCash (ZHChain) Ecosystem

The **ZHCash (ZHChain) testnet** is a critical component of the blockchain infrastructure, providing a secure and controlled environment for development, testing, and deployment of new features before they reach the main network (mainnet). It plays a key role in ensuring the **stability, reliability, and security** of the entire ecosystem.

---

## Why Is the Testnet Important?

The testnet is a duplicate network, technically identical to the mainnet, but without any real financial value. It enables developers and node operators to:

🔬 **Develop and debug**

* Test new features and protocol upgrades
* Validate smart contracts, transactions, and consensus logic
* Simulate various network scenarios

🧪 **Experiment and research**

* Conduct load testing and performance analysis
* Evaluate scalability under different conditions
* Test innovative solutions without real-world risk

🛡 **Mitigate risks**

* Prevent bugs and vulnerabilities from affecting the mainnet
* Identify weaknesses and ensure proper fixes
* Prepare updates without exposing users' assets to danger

---

## How Does the ZHCash Testnet Work?

The ZHCash testnet:

* Has its own independent blockchain and genesis block
* Uses separate ports and a different network identifier
* Operates with test coins that have no market value
* Can be restarted or reset as needed for protocol changes

---

## Who Uses the Testnet?

* **Developers** — for building and testing smart contracts, apps, and wallets
* **Validators & Node Operators** — to validate setup, sync, and stability
* **Security Researchers** — to explore vulnerabilities and network behavior
* **Community Members** — to preview and test upcoming features

---

## Impact on the ZHCash Ecosystem

📈 **Quality Assurance**
Only tested, stable solutions are deployed on the mainnet.

⚙️ **Continuous Innovation**
Ongoing development and upgrades are made possible without disrupting the live chain.

🤝 **Transparency**
Open access to testnet fosters collaboration and trust among developers and the wider community.

---

## Conclusion

The **ZHCash (ZHChain) testnet** is not just a sandbox — it's a **foundation for sustainable innovation**. It enables low-risk experimentation, supports developer engagement, and ensures a robust and secure environment for the evolution of the ZHCash ecosystem.

---

If you'd like, I can help convert this article into a PDF, Webflow blog post, GitHub Wiki format, or a social media version with emojis and hashtags.


Doc by GRAViTON
