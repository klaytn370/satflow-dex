# SatFlow DEX

SatFlow DEX is a minimal but proper AMM-based decentralized exchange built on **OP_NET (Bitcoin Layer 1)**.

It implements a two-token liquidity pool using the **constant product formula (x * y = k)**, allowing users to:
- Add liquidity
- Remove liquidity
- Swap tokens
in a trust-minimized way.

This project is built as part of the **OP_NET Vibecoding Challenge** using Bob (OP_NET MCP) and OpenClaw.

---

## 🧠 How It Works (High Level)

- The pool holds two OP20 tokens: `TokenA` and `TokenB`
- Liquidity providers deposit both tokens and receive LP shares
- Swaps follow the formula: **reserveA * reserveB = k**
- A small fee is applied on swaps (e.g. 0.3%)
- LP shares represent proportional ownership of the pool

---

Structure
---

## 📜 Smart Contract

Main contract:

- `contracts/SatFlowPool.opnet`

Core functions:

- `addLiquidity(amountA, amountB)`
- `removeLiquidity(lpShares)`
- `swapAforB(amountIn)`
- `swapBforA(amountIn)`

---

## 🗺️ Roadmap

See [docs/roadmap.md](docs/roadmap.md) for planned improvements.

---

## 🤝 Contributing

Contributions are welcome!  
Please read [CONTRIBUTING.md](CONTRIBUTING.md) to get started.

---

## 🔐 Security

Please read [SECURITY.md](SECURITY.md) for responsible disclosure guidelines.

---

## 📜 Changelog

See [CHANGELOG.md](CHANGELOG.md) for release history.

---

## 📄 License

This project is licensed under the terms of the [LICENSE](LICENSE) file.
