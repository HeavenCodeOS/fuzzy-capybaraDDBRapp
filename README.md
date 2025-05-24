# TheeForestKingdom.vaults

A decentralized, KYC-enabled vault platform for USDC custody and fiat payouts (e.g., Cash App), with integrated frontend, backend, and Ethereum contracts.

---

## Quickstart

### 1. Smart Contracts

- Edit `.env` with your keys
- Deploy Membership and Vault contracts:
  ```
  cd blockchain
  npm install
  npx hardhat run scripts/deploy.js --network mainnet
  ```
- Update `metadata.json` and backend/frontend `.env` with contract addresses

### 2. Backend

- Copy `.env.example` to `.env`, fill values
- Install: `npm install`
- Start: `node server.js`

### 3. Frontend

- `cd frontend`
- `npm install`
- Copy `.env.example` to `.env`, set API and contract addresses
- `npm run dev` (or deploy with Vercel)

### 4. Registration

- Obtain JWT via `/api/auth/login`
- Register with:
  ```
  curl -X POST https://your.domain/api/register \
    -H "Authorization: Bearer YOUR_JWT" \
    -d @metadata.json
  ```

### 5. Usage

- Connect MetaMask
- Complete KYC
- Deposit/withdraw USDC, request fiat payout to Cash App

---

## See BUILD_GUIDE.md for full step-by-step instructions