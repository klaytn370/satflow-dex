# SatFlow DEX

![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-prototype-blue.svg)

SatFlow DEX is a minimal but proper AMM-based decentralized exchange built on **OP_NET (Bitcoin Layer 1)**.  
It uses the **constant product formula (x * y = k)** to enable trust-minimized swaps between two OP20 tokens.

This project was built with the help of **Bob (OP_NET MCP)** and **OpenClaw** as part of the **OP_NET Vibecoding Challenge**.

---

## ✨ Features

- 🔁 Two-token AMM pool (OP20 tokens)
- 📈 Constant product pricing formula (x * y = k)
- 💧 Add liquidity
- 💧 Remove liquidity
- 🔄 Swap Token A ↔ Token B
- 🪙 LP share tracking
- 🧠 Minimal, hackathon-friendly design

---

## 🧠 How It Works (High Level)

- The pool holds two OP20 tokens: TokenA and TokenB
- Liquidity providers deposit both tokens and receive LP shares
- Swaps follow the formula:  
  **reserveA * reserveB = k**
  - A small fee is applied on swaps (example: 0.3%)
  - LP shares represent proportional ownership of the pool

  ---

  ## 📜 Smart Contract

  Main contract:
  - `contracts/SatFlowPool.opnet`

  Core functions:
  - `addLiquidity(amountA, amountB)`
  - `removeLiquidity(shareAmount)`
  - `swapAforB(amountAIn)`
  - `swapBforA(amountBIn)`

  > Note: This is a prototype focused on core AMM logic for hackathon and educational purposes.

  ---

  ## 📚 Documentation

  - [Architecture](docs/architecture.md)
  - [Roadmap](docs/roadmap.md)

  ---

  ## 🚀 Getting Started

  1. Clone the repository
  2. Open in GitHub Codespaces
  3. Explore `contracts/SatFlowPool.opnet`
  4. Adapt OP20 calls to official OP_NET APIs if needed
  5. Build and deploy using OP_NET tooling

  ---

  ## 🤖 Built With

  - OP_NET (Bitcoin Layer 1)
  - Bob (OP_NET MCP)
  - OpenClaw
  - GitHub Codespaces

  ---

  ## ⚠️ Disclaimer

  This project is an experimental prototype.  
  Do **NOT** use with real funds without proper security reviews.

  ---

  ## ❤️ Credits

  Built with the help of Bob (OP_NET MCP) and OpenClaw.