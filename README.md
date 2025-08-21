# Horizons-Lit

## An Experimental Integration of Meta Horizons with Lit Protocol for NFT Purchases

This repository contains an experimental integration between Meta Horizons and Lit Protocol, enabling secure, decentralized NFT purchase capabilities within the Horizons ecosystem.

## Overview

Horizons-Lit combines Meta Horizons' immersive social experiences with Lit Protocol's decentralized access control infrastructure. This integration allows users to securely purchase, manage, and verify ownership of NFTs within the Horizons metaverse.

## Features

- Decentralized authentication for NFT purchases
- Secure access control for exclusive Horizons content
- Encrypted, verifiable ownership credentials
- Seamless integration with existing Horizons experiences
- Cross-chain compatibility for NFT marketplaces

## Getting Started

### Prerequisites

- Node.js (v14 or later)
- Meta Horizons developer account
- Lit Protocol SDK access
- Web3 wallet (MetaMask recommended)

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/horizons-lit.git
cd horizons-lit

# Install dependencies
npm install

# Configure environment
cp .env.example .env
# Edit .env with your API keys and configuration
```

## Usage

### Basic Integration

```javascript
import { HorizonsLit } from 'horizons-lit';

// Initialize the integration
const horizonsLit = new HorizonsLit({
    litNodeClient: yourLitNodeClient,
    horizonsApiKey: process.env.HORIZONS_API_KEY
});

// Connect user wallet
await horizonsLit.connect(userWalletAddress);

// Verify NFT ownership
const hasAccess = await horizonsLit.verifyNftOwnership(nftContractAddress, tokenId);
```

### Purchase Flow

```javascript
// Initiate NFT purchase
const purchaseSession = await horizonsLit.createPurchaseSession({
    nftCollection: 'horizons-exclusive',
    tokenId: '123',
    price: '0.1'  // ETH
});

// Complete purchase with Lit Protocol verification
const purchaseResult = await horizonsLit.completePurchase(purchaseSession.id);
```

## Documentation

For detailed documentation, see the [Wiki](https://github.com/yourusername/horizons-lit/wiki).

## Project Structure

```
horizons-lit/
├── src/                # Source code
│   ├── auth/           # Authentication handlers
│   ├── lit/            # Lit Protocol integration
│   ├── horizons/       # Meta Horizons API wrappers
│   └── nft/            # NFT purchase and verification
├── examples/           # Example implementations
├── tests/              # Test suite
└── docs/               # Documentation
```

## Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This is an experimental integration and may contain bugs or security vulnerabilities. Use at your own risk in non-production environments only.

## Acknowledgements

- [Meta Horizons Team](https://about.meta.com/metaverse/)
- [Lit Protocol](https://litprotocol.com/)
- All contributors to this project