contract address :
<img width="1883" height="881" alt="image" src="https://github.com/user-attachments/assets/8d96b807-8877-42b8-9b45-9bc0f4f5987e" />

UI Screenshot :
<img width="1895" height="901" alt="image" src="https://github.com/user-attachments/assets/79e73460-b285-46a7-b9d3-139dd0abd2b0" />


CI/CD pipeline badge : <img width="1862" height="630" alt="image" src="https://github.com/user-attachments/assets/cad7c3b9-a072-435a-b7f2-a6538275aee5" />


Live Demo Link : https://insurance-claims-syste-git-main-nishant-kumar-s-projects16.vercel.app


 mobile responsive view : 

 
 <img width="400" height="1568" alt="image" src="https://github.com/user-attachments/assets/4c8a71e4-9278-4eca-adb8-85a83968b3da" />





# 🛡️ ClaimChain - Decentralized Insurance Claims System

## 📌 Project Description
Traditional insurance is plagued by centralized gatekeepers — adjusters, administrators, and executives who decide whether your claim gets paid, and when. ClaimChain eliminates all of that.

Built on Stellar Soroban, ClaimChain is a decentralized application (DApp) where insurance claims are filed, reviewed, and paid out entirely on-chain through community consensus. There is no owner, no admin role, and no privileged address — the smart contract is permissionless by design.

Claimants stake a small amount of XLM when filing, which deters spam. The broader community votes on claim validity. Once voting ends, anyone can trigger resolution and payout — the contract enforces the outcome automatically.

## ⚙️ What It Does
- Fund the insurance pool — anyone can contribute XLM
- File a claim with title, description, evidence URI, and amount
- Vote on claims (approve/reject) during a 3-day window
- Resolve claims once voting ends and quorum is met
- Execute payouts for approved claims
- Reclaim 50% stake for rejected claims

## ✨ Features

### Core
- Fully permissionless (no owner, no admin)
- Community voting with quorum and threshold
- Trustless automatic payouts
- Stake-based spam deterrence
- Voter rewards (1% of claim)
- Evidence via IPFS/URLs
- Open funding pool

### DApp Frontend
- Freighter wallet integration
- Live on-chain data via Soroban RPC
- Explorer links (Stellar Expert)
- Terminal-style UI (IBM Plex Mono)
- Responsive design

### Contract Mechanics
- Voting Period: 3 days
- Minimum Quorum: 3 votes
- Approval Threshold: 60%
- Claimant Stake: 0.01 XLM
- Max Claim Amount: 10,000 XLM
- Voter Reward: 1% (split equally)
- Rejected Stake Returned: 50%

## 🔄 How It Works
1. User files a claim with 0.01 XLM stake
2. 3-day voting window starts
3. Community votes approve/reject
4. After voting ends, anyone calls resolve_claim()
5. If 60% or more approve, payout executed
6. If less than 60% approve, 50% stake returned

## 📜 Smart Contract
- **Contract Address:** CBX74DY3MEWPQEOWERWMTN7WOLA3YC7HQLA7IT64R7K5YCBKIJHBM2VW
- **Network:** Stellar Testnet
- **Live Demo:** https://insurance-claims-syste.vercel.app

## 🔑 Key Contract Files
- [lib.rs (Smart Contract)](https://github.com/Nishantk16/Insurance-Claims-Syste/blob/main/contract/contracts/contract/src/lib.rs)
- [Cargo.toml](https://github.com/Nishantk16/Insurance-Claims-Syste/blob/main/contract/contracts/contract/Cargo.toml)
- [Makefile](https://github.com/Nishantk16/Insurance-Claims-Syste/blob/main/contract/contracts/contract/Makefile)
- [Cargo.lock](https://github.com/Nishantk16/Insurance-Claims-Syste/blob/main/contract/Cargo.lock)
- [contract.ts (Frontend Integration)](https://github.com/Nishantk16/Insurance-Claims-Syste/blob/main/client/hooks/contract.ts)

- ### contract.ts Key Code
```typescript
import { Contract, Networks, TransactionBuilder, rpc } from "@stellar/stellar-sdk";

export const CONTRACT_ADDRESS = "CA43I2DUWKVEMKEFKNRNACVVKJYHN6SLJ6B6GACIV5SC3GUC6APWDSXN";
export const NETWORK_PASSPHRASE = Networks.TESTNET;
export const RPC_URL = "https://soroban-testnet.stellar.org";

// Functions: fileClaim, vote, resolveClaim, getClaim, getVoteStats
```

## 🛠️ Tech Stack
- Rust, Soroban SDK
- Stellar Testnet
- Soroban RPC
- Next.js, TypeScript, Tailwind CSS
- @stellar/stellar-sdk
- Freighter Wallet
- IPFS
- Stellar Expert

## 🚀 Getting Started

### Prerequisites
- Freighter wallet installed
- Stellar Testnet account with XLM
- Modern browser

### Run Locally
git clone https://github.com/Nishantk16/Insurance-Claims-Syste
cd Insurance-Claims-Syste
cd client
npm install
npm run dev

## 📐 Contract Functions

### Read Functions
- get_all_claims()
- get_claim(id)
- get_pool_balance()
- get_voters(id)
- get_voting_status(id)

### Write Functions
- contribute()
- file_claim(title, description, evidence_uri, amount)
- vote(claim_id, approve)
- resolve_claim(claim_id)
- execute_payout(claim_id)
- reclaim_stake(claim_id)

## 🔓 Permissionless Design
- No owner or admin roles
- No whitelist system
- Anyone can resolve claims
- Anyone can execute payouts
- Anyone can reclaim stake
- Economic incentives replace moderation
- Time-based rules enforced by smart contract

## 👥 User Feedback
We are onboarding testnet users to improve ClaimChain!

👉 Fill out our feedback form: https://docs.google.com/forms/d/e/1FAIpQLSc3kZlOxoRcCHYj-njzyPynmGXaL3dFjX2ytfSwXKXQkngW1w/viewform?usp=publish-editor

### How to test ClaimChain:
1. Visit https://insurance-claims-syste.vercel.app
2. Connect your Stellar testnet wallet
3. File a claim or vote on existing claims
4. Fill out the feedback form above
