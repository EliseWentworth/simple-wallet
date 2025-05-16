# Simple Wallet for Art.AI

A secure and user-friendly wallet implementation for the Art.AI ecosystem on Solana blockchain. This wallet enables seamless interaction with Art.AI's NFT minting, DAO governance, and decentralized art creation features.

## Features

- **Wallet Management**
  - Create new wallets with secure key generation
  - Import existing wallets via seed phrase or private key
  - Export wallet credentials with encryption
  - Sign transactions for Art.AI interactions

- **Solana Network Integration**
  - Connect to Solana mainnet and testnet
  - Check SOL and SPL token balances
  - Send transactions with minimal fees ($0.0025)
  - Real-time transaction status tracking

- **Art.AI Smart Contract Integration**
  - Mint NFTs from AI-generated artwork
  - Create and vote on DAO proposals
  - Participate in community governance
  - Track on-chain reputation and rewards

- **User Interface**
  - Intuitive wallet management dashboard
  - Transaction history and status monitoring
  - Art.AI interaction panel for NFT and DAO features
  - Mobile-responsive design

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/simple-wallet-for-art-ai.git

# Install dependencies
cd simple-wallet-for-art-ai
npm install

# Build the project
npm run build

# Start the development server
npm run dev
```

## Usage Examples

### Create a New Wallet

```typescript
import { createWallet } from './src/wallet';

const wallet = await createWallet();
console.log('New wallet address:', wallet.publicKey.toString());
```

### Mint an NFT

```typescript
import { mintNft } from './src/artAi';

const nftMetadata = {
  name: 'AI Generated Artwork',
  description: 'Created using Art.AI',
  image: 'arweave://...'
};

const nft = await mintNft(wallet, nftMetadata);
console.log('Minted NFT:', nft.mintAddress);
```

### Create a DAO Proposal

```typescript
import { createProposal } from './src/artAi';

const proposal = await createProposal({
  title: 'New Art Style Implementation',
  description: 'Add cyberpunk style to AI generation',
  voteEndTime: new Date(Date.now() + 7 * 24 * 60 * 60 * 1000)
});

console.log('Proposal created:', proposal.id);
```

## Architecture

```
simple-wallet-for-art-ai/
├── src/
│   ├── wallet/       # Core wallet functionality
│   ├── solana/       # Solana network interactions
│   ├── artAi/        # Art.AI smart contract integration
│   └── ui/           # User interface components
├── tests/            # Unit and integration tests
└── docs/             # Documentation
```

## Testing

```bash
# Run all tests
npm test

# Run specific test suite
npm test wallet
npm test solana
npm test artAi
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

MIT License - see the [LICENSE](LICENSE) file for details

## Contact

Project Link: [https://github.com/yourusername/simple-wallet-for-art-ai](https://github.com/yourusername/simple-wallet-for-art-ai)

## Acknowledgments

- [Art.AI Protocol](https://art.ai)
- [Solana](https://solana.com)
- [Arweave](https://arweave.org)