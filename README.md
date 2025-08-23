# ChariBlock 🔗

> A decentralized charity platform built on Ethereum — making every donation transparent, secure, and trustworthy.

---

## What is ChariBlock?

ChariBlock lets donors give cryptocurrency directly to verified charities. Every transaction is recorded on the blockchain, so anyone can verify where funds go — no middlemen, no hidden fees, full accountability.

---

## Features

**For Donors**

- Connect MetaMask wallet and donate instantly
- Browse KYC-verified charity campaigns
- Get blockchain transaction hash as donation proof
- Track your full donation history

**For Charities**

- Launch fundraising campaigns on-chain
- Submit KYC documents for verification
- Receive funds directly to your wallet

**For Admins**

- Review and approve charity applications
- Monitor platform activity via analytics dashboard
- Emergency controls and platform fee management

---

## Tech Stack

| Layer           | Technologies                                     |
| --------------- | ------------------------------------------------ |
| Frontend        | Next.js 14, TypeScript, Tailwind CSS, shadcn/ui  |
| Blockchain      | Web3.js / Ethers.js, MetaMask SDK                |
| Backend         | Django 4.2, Django REST Framework, PostgreSQL    |
| Storage         | Pinata (IPFS)                                    |
| Smart Contracts | Solidity, Hardhat, OpenZeppelin, Sepolia Testnet |

---

## Getting Started

### Prerequisites

- Node.js v16+
- Python v3.8+
- MetaMask browser extension
- Git

---

### 1. Clone the repo

```bash
git clone https://github.com/kushal2060/Charity-Donation-BLOCKCHAIN-System
```

---

### 2. Frontend Setup

```bash
npm install
cp .env.example .env.local
npm run dev
```

Configure `.env.local`:

```env
NEXT_PUBLIC_BACKEND_API=http://localhost:8000/api
NEXT_PUBLIC_CONTRACT_ADDRESS=your_contract_address
NEXT_PUBLIC_CHAIN_ID=11155111
```

Visit `http://localhost:3000`

---

### 3. Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Configure `.env`:

```env
SECRET_KEY=your-secret-key
DEBUG=True
PINATA_API_KEY=your-pinata-api-key
PINATA_SECRET_KEY=your-pinata-secret
CORS_ALLOWED_ORIGINS=http://localhost:3000
```

API runs at `http://localhost:8000`

---

### 4. Smart Contracts Setup

```bash
cd contracts
npm install
cp .env.example .env
npx hardhat compile
npm run test
```

Configure `.env`:

```env
PRIVATE_KEY=your-wallet-private-key
SEPOLIA_RPC_URL=https://eth-sepolia.g.alchemy.com/v2/YOUR-API-KEY
ETHERSCAN_API_KEY=your-etherscan-api-key
```

Deploy:

```bash
# Local
npx hardhat node
npm run deploy:local

# Sepolia Testnet
npm run deploy:sepolia
```

---

## Security

- ReentrancyGuard against reentrancy attacks
- Pausable contracts for emergency stops
- Role-based access control
- KYC verification required for charities
- Funds sent directly to charity wallets — never held by the platform
