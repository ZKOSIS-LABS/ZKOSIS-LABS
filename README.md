

# 🛡️ ZKOSIS

We’re not launching additional MCP servers—there’s already a robust collection in operation. Instead, we’re focusing on building the infrastructure layer that allows these existing servers to be seamlessly accessed via our free ZKOSIS client (available at labs.zkosis.com). Think of ZKOSIS as a universal launchpad or gateway, enabling users to remotely connect and interact with any MCP server—no need to self-host or maintain complex setups.
Key Highlights

    Infrastructure over duplication
    We leverage the existing MCP server ecosystem rather than expanding it. MCP servers are already widely available across tools and platforms .

    A seamless remote bridge
    ZKOSIS functions as a unified interface: discover, connect, authorize (OAuth, API keys), and invoke capabilities across any MCP server—all from one client.

    Simplified tool access
    Whether it's code deployments, cloud operations, or data integration, users get plug‑and‑play MCP functionality without setup hassles

---

## 🧠 Core Features

* **Model Context Protocol (MCP) Server**
  The MCP Server receives user inputs, runs predictive inference, and creates zk-SNARK proofs (Groth16/PLONK). These proofs are verified and attested via smart contracts on Ethereum, ensuring trustless computation.

* **ZKOSIS API & LLM Integration**
  Seamlessly automates blockchain interactions—from invoking contracts to logging verification events on Etherscan-compatible explorers.

* **Verifiable On-Chain AI**
  Every output is anchored on-chain with full integrity, ensuring trustless, encrypted transparency.

---

## 🧩 Architecture Overview

```
User Input 
    ↓
[MCP Server → ezkl Inference → ZK Proof]
    ↓
Verifier.sol + AttestManager.sol
    ↓
⛓ On-chain log (Etherscan-compatible)
```

---

## 🚀 Getting Started

### Prerequisites:

* Node.js ≥ 18 or Bun ≥ 1.0
* Yarn or npm

### Installation & Setup

```bash
git clone https://github.com/zkosis/evm-mcp-server.git
cd evm-mcp-server

# Install dependencies
npm install
```

### Running the MCP Server

* **StdIO mode**:

  ```bash
  npx @zkosis/evm-mcp-server --stdio
  ```

* **HTTP mode (with Server-Sent Events)**:

  ```bash
  npx @zkosis/evm-mcp-server --http
  ```

### Supported Chains

Works across 30+ EVM-compatible chains, including Ethereum, Optimism, Arbitrum, Base, Polygon, Avalanche, zkSync Era, and more.

---

## ⚙️ Usage Examples

### Check an ERC20 Token Balance

```js
const res = await mcp.invokeTool("get-token-balance", {
  tokenAddress: "USDC_contract",
  ownerAddress: "vitalik.eth",
  network: "ethereum"
});
console.log(res.formatted); // e.g., "1000"
```

### Run a Transfer

```js
const res = await mcp.invokeTool("transfer-token", {
  privateKey: "0x…",
  tokenAddress: "0x…",
  toAddress: "0x…",
  amount: "50",
  network: "polygon"
});
console.log(res.txHash);
```

---

## 🔒 Security & Proof

* Private keys are used only for signing and are never stored locally.
* zk-SNARK systems (Groth16/PLONK) ensure verifiable, zero-knowledge attestations.
* HTTPS and rate-limiting best practices applied.

---

## 📦 ZKOSIS NPM Package

Install the EVM MCP Server module:

```bash
npm install @zkosis/evm-mcp-server@1.1.3
```

(Current version **1.1.3** released on June 15, 2025.)

---

## 🌐 Ecosystem & Impact

* 30+ validators and integrations across 40+ blockchains.
* Prototype implementations have shown \~25% average ROAS uplift.
* Public attestation through Etherscan-compatible logs enhances transparency.

---

## 📚 Documentation & Support

* Detailed docs on MCP server, API, and tools are included in the NPM package and available on the ZKOSIS website.
* Follow our Twitter/X, Telegram, and GitBook for updates.

---

## 🛠️ Developer Contribution

We welcome contributors! Here's how to help:

* Add new chain support in `src/core/chains.ts`
* Register tools in `src/core/tools.ts`
* Extend services in `src/core/services/`
* Submit PRs for bug fixes, documentation improvements, and new features

---

## 📄 License

MIT License — feel free to use, modify, and contribute!

---

## 🚀 Join the Future

Bring encrypted, verifiable AI inference to your dApps with **ZKOSIS**.
Explore our GitHub, integrate the MCP server, and help lead the next wave of blockchain innovation.

---

*© 2025 ZKOSIS. Privacy Policy available on [zkosis.com](https://zkosis.com).*

---

