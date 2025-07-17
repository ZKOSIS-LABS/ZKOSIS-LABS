🛡️ ZKOSIS: Zero‑Knowledge AI Attestation for Ethereum

ZKOSIS is a next-gen compute protocol combining AI inference, zk‑SNARK proofs, and smart contract attestation in a modular, trustless architecture. It enables encrypted, on‑chain verification of AI-powered predictions.
🧠 Core Features

    **Model Context Protocol (MCP) Server**
    Receives user inputs, runs predictive inference, and creates zk‑SNARK proofs (Groth16/PLONK).
    Proofs are verified and attested via smart contracts on Ethereum.
    mcpworld+2zkosis.com+2Libraries.io+2

    ZKOSIS API & LLM Integration
    Seamlessly automates blockchain interactions — from invoking contracts to logging verification events on Etherscan‑compatible explorers.

    Verifiable On‑Chain AI
    Every output is anchored on‑chain with full integrity, ensuring trustless, encrypted transparency.
    Libraries.io+4zkosis.com+4Moralis | Enterprise-Grade Web3 APIs+4

🧩 Architecture Overview

User Input 
    ↓
[MCP Server → ezkl Inference → ZK Proof]
    ↓
Verifier.sol + AttestManager.sol
    ↓
⛓ On‑chain log (Etherscan‑compatible)

🚀 Getting Started
Prerequisites:

    Node.js ≥ 18 or Bun ≥ 1.0

    Yarn or npm

Installation & Setup

git clone https://github.com/zkosis/evm-mcp-server.git
cd evm-mcp-server

# Install dependencies
npm install

Running the MCP Server

    StdIO mode:

npx @zkosis/evm-mcp-server --stdio

HTTP mode (with Server-Sent Events):

    npx @zkosis/evm-mcp-server --http

Supported Chains

Works across 30+ EVM-compatible chains including Ethereum, Optimism, Arbitrum, Base, Polygon, Avalanche, zkSync Era, and more
Libraries.io
.
⚙️ Usage Examples
Check an ERC20 Token Balance

const res = await mcp.invokeTool("get-token-balance", {
  tokenAddress: "USDC_contract",
  ownerAddress: "vitalik.eth",
  network: "ethereum"
});
console.log(res.formatted); // e.g. "1000"

Run a Transfer

const res = await mcp.invokeTool("transfer-token", {
  privateKey: "0x…",
  tokenAddress: "0x…",
  toAddress: "0x…",
  amount: "50",
  network: "polygon"
});
console.log(res.txHash);

🔒 Security & Proof

    Private keys are used only for signing and are never stored. Security best practices are followed, including HTTPS and rate‑limiting
    Libraries.io
    .

    zk‑SNARK systems (Groth16/PLONK) ensure verifiable, zero‑knowledge attestations.

📦 ZKOSIS NPM Package

Install the EVM MCP Server module:

npm install @zkosis/evm-mcp-server@1.1.3

Current version 1.1.3 released on June 15, 2025
zkosis.com
Libraries.io+1mcpworld+1
.
🌐 Ecosystem & Impact

    30+ validators and integrations across 40+ blockchains.

    Prototype implementations show ~25% average ROAS uplift
    apespace.io+4zkosis.com+4Libraries.io+4
    .

    Public attestation through Etherscan‑compatible logs promotes transparency and accountability.

📚 Documentation & Support

    Detailed documentation on MCP server, API, tools, and resource URIs is available in the NPM package
    zkosis.com
    Libraries.io+1mcpworld+1
    .

    Follow us on Twitter/X, Telegram, and our Gitbook for updates.

🛠️ Developer Contribution

Contributions are welcome! Guidelines:

    Add new chain/network support in src/core/chains.ts

    Register tools in src/core/tools.ts

    Extend services in src/core/services/

    Create PRs for fixes, docs, enhancements

📄 License

MIT license — feel free to use and contribute!
🚀 Join the Future

Bring encrypted, verifiable AI inference to your dApps with ZKOSIS.
Explore our GitHub, integrate the MCP server, and lead the next wave of blockchain innovation.

© 2025 ZKOSIS. Privacy Policy available on zkosis.com.
