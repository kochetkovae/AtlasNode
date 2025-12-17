# AtlasNode

Built for Base

AtlasNode is a Base-first repository intended to validate that a Base RPC endpoint and wallet onboarding flow behave correctly in a browser environment.

It is optimized for quick checks: pick a Base network, connect a wallet, run reads, and cross-reference results on Basescan.

## Networks

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  
RPC: https://mainnet.base.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  
RPC: https://sepolia.base.org  

## What AtlasNode Does

Primary file: app/atlasNode.ts

The app:
- Initializes an OnchainKitProvider tied to the selected Base chain
- Presents wallet connection UI via OnchainKit
- Uses Viem to perform read-only calls:
  - getChainId
  - getBlockNumber
  - getBalance (native ETH) for a supplied address
- Keeps Basescan explorer context visible

## Repository Structure

app/  
- atlasNode.ts  
  React component wiring wallet UX with Base JSON-RPC reads.

Common supporting files:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

## Libraries

OnchainKit  
https://github.com/coinbase/onchainkit  

Viem  
EVM client for Base JSON-RPC reads  

## Installation and Running

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies using your preferred package manager and run with a standard React/Vite or Next.js dev server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

## License

MIT License

## Author

Public contact (email): feed_haggle0v@icloud.com

GitHub: https://github.com/kochetkovae 

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract address:  
0x0b346bf911a8754e3454c610287174fba8ab521a

Deployment and verification:
- https://sepolia.basescan.org/address/0x0b346bf911a8754e3454c610287174fba8ab521a
- https://sepolia.basescan.org/0x0b346bf911a8754e3454c610287174fba8ab521a/0#code  
