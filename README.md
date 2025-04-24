# NFT Marketplace Contracts – ERC-721 with IPFS Metadata and Admin Roles

This project is a smart contract suite for an NFT Marketplace, focusing on ERC-721 tokens with IPFS-hosted metadata. It includes a robust admin role system and upgradeable contract architecture.

## 🛠️ Features

- 🔹 ERC-721 compliant NFT contract
- 🖼️ Metadata stored on IPFS
- 🛡️ Role-based access control (e.g., `ADMIN_ROLE`, `MINTER_ROLE`)
- 🚀 Upgradeable architecture using OpenZeppelin Upgrades
- 🧪 Hardhat tests and deployment scripts included

## 📁 Structure

contracts/ ├── NFT.sol # Core ERC-721 NFT contract with IPFS support ├── Marketplace.sol # Marketplace logic (optional for extension) ├── AccessControl.sol # Custom or inherited access control scripts/ ├── deploy.js # Deployment logic using Hardhat test/ ├── NFT.test.js # Unit tests for NFT features


## 🧱 Tech Stack

- Solidity (v0.8.x)
- Hardhat
- OpenZeppelin Contracts
- IPFS (via Pinata or Web3.Storage)
- Ethers.js

## 🚀 Deployment

```

```


## 🧪 Testing

```
npx hardhat test
```

## 🔐 Roles Example

```solidity
bytes32 public constant ADMIN_ROLE = keccak256("ADMIN_ROLE");
bytes32 public constant MINTER_ROLE = keccak256("MINTER_ROLE");

constructor() {
    _setupRole(DEFAULT_ADMIN_ROLE, msg.sender);
    _setupRole(ADMIN_ROLE, msg.sender);
}
```
