# ChariBlock - Decentralized Blockchain Charity Platform

## Overview

**ChariBlock** is a blockchain-based charity platform that brings **transparency**, **security**, and **trust** to charitable donations. Built on Ethereum, ChariBlock ensures every donation is tracked on-chain, providing donors with complete visibility and accountability.

## Features

### For Donors

- **MetaMask Wallet Integration** - Connect and donate with Web3 wallets
- **Browse Verified Charities** - Explore KYC-verified charity campaigns
- **Instant Donations** - Make secure cryptocurrency donations
- **Donation Receipts** - Get blockchain transaction hashes as proof
- **Donation History** - Track all your charitable contributions

### For Charity Organizations

- **Create Charity Campaigns** - Launch fundraising campaigns on-chain
- **KYC Verification** - Submit documents for legitimacy verification
- **IPFS Document Storage** - Secure, decentralized document management
- **Direct Fund Receipt** - Receive donations directly to your wallet

### For Platform Admins

- **Charity Verification System** - Review and approve charity applications
- **Document Verification** - Access uploaded KYC documents
- **Platform Controls** - Manage platform fee and emergency controls
- **Analytics Dashboard** - Monitor platform activity and statistics

---

## Tech Stack

### Frontend

- **Next.js 14** - React framework for production
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first CSS framework
- **shadcn/ui** - Beautiful, accessible UI components
- **Web3.js / Ethers.js** - Ethereum blockchain interaction
- **MetaMask SDK** - Wallet connection

### Backend

- **Django 4.2** - Python web framework
- **Django REST Framework** - RESTful API
- **SQLite/PostgreSQL** - Database
- **Pinata** - IPFS file storage
- **CORS** - Cross-origin resource sharing

### Blockchain

- **Solidity** - Smart contract programming
- **Hardhat** - Ethereum development environment
- **OpenZeppelin** - Secure smart contract library
- **Sepolia Testnet** - Ethereum test network
- **Etherscan** - Blockchain explorer integration

---

## Quick Start

### Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v16 or higher)
- **Python** (v3.8 or higher)
- **npm** or **yarn**
- **MetaMask** browser extension
- **Git**

### 1. Clone the Repository

```bash
git clone https://github.com/kushal2060/Charity-Donation-BLOCKCHAIN-System

```

### 2. Frontend Setup (Next.js)

```bash
# Install dependencies
npm install

# Create environment file
cp .env.example .env.local

# Configure environment variables in .env.local
# NEXT_PUBLIC_BACKEND_API=http://localhost:8000/api
# NEXT_PUBLIC_CONTRACT_ADDRESS=your_deployed_contract_address
# NEXT_PUBLIC_CHAIN_ID=11155111 # Sepolia testnet

# Run development server
npm run dev
```

Visit `http://localhost:3000` to see the application.

### 3. Backend Setup (Django)

```bash
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On macOS/Linux:
source venv/bin/activate
# On Windows:
# venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Setup database
python manage.py migrate

# Create superuser for admin access
python manage.py createsuperuser

# Run development server
python manage.py runserver
```

The API will be available at `http://localhost:8000`

### 4. Smart Contract Setup (Hardhat)

```bash
cd contracts

# Install dependencies
npm install

# Create environment file
cp .env.example .env

# Configure .env with your settings:
# PRIVATE_KEY=your_wallet_private_key
# SEPOLIA_RPC_URL=your_alchemy_or_infura_url
# ETHERSCAN_API_KEY=your_etherscan_api_key

# Compile contracts
npx hardhat compile

# Run tests
npm run test

# Deploy to local network
npx hardhat node  # In separate terminal
npm run deploy:local

# Deploy to Sepolia testnet
npm run deploy:sepolia
```

---

## Security Features

- **ReentrancyGuard** - Prevents reentrancy attacks
- **Pausable Contracts** - Emergency stop mechanism
- **Access Control** - Role-based permissions
- **Input Validation** - Comprehensive parameter checks
- **Direct Transfers** - Funds sent directly to charity wallets
- **IPFS Storage** - Decentralized document storage
- **KYC Verification** - Admin approval required

---

## Environment Variables

### Frontend (.env.local)

```env
NEXT_PUBLIC_BACKEND_API=http://localhost:8000/api
NEXT_PUBLIC_CONTRACT_ADDRESS=0x...
NEXT_PUBLIC_CHAIN_ID=11155111
```

### Backend (.env)

```env
SECRET_KEY=your-secret-key
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
CORS_ALLOWED_ORIGINS=http://localhost:3000
PINATA_API_KEY=your-pinata-api-key
PINATA_SECRET_KEY=your-pinata-secret
```

### Contracts (.env)

```env
PRIVATE_KEY=your-wallet-private-key
SEPOLIA_RPC_URL=https://eth-sepolia.g.alchemy.com/v2/YOUR-API-KEY
ETHERSCAN_API_KEY=your-etherscan-api-key
```

---
