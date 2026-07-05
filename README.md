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
- **Contract Address:** CB6X2N33IW2JJQWBNKL3CWKCPCS7CCBHSDDQPIKEO2F7LRG6BFTWWOSB
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

📊 Full form responses (Excel/Sheet): https://docs.google.com/spreadsheets/d/1WO_F7pDY_UZPfbAEH0i_oZIz64cJEeKh-1x-n3-AvEg/edit?usp=drivesdk

### How to test ClaimChain:
1. Visit https://insurance-claims-syste.vercel.app
2. Connect your Stellar testnet wallet
3. File a claim or vote on existing claims
4. Fill out the feedback form above

## 🧑‍🤝‍🧑 Users Onboarded

We onboarded 10 testnet users who actively used ClaimChain's core flows (file claim, browse claims, vote, submit evidence, resolve claim) and submitted feedback.

| # | Name | Email | Wallet Address | Feedback Given |
|---|------|-------|-----------------|-----------------|
| 1 | Mandavi Kumari | mandavikumari185@gmail.com | GBQ54XUHUOO3ZD27ZHCONISXC3N2O5MAALJCMEI63FDJBGIZZDRYVVD7 | Yes |
| 2 | Ayush Rai | raiiayush007@gmail.com | GCY4G2WFUANO2VIRXTUPEWJUO55PNK54XSDKOJHLGTC6S7AJ2YXK4HEZ | Yes |
| 3 | Roshan Gupta | 2005guptaroshan@gmail.com | GCWYDBWDWA2GZMWVBHDDQW27XXQNF5BEYBLPJ6IQSFLR474FRFXWTH3U | Yes |
| 4 | Md Sadique | sadiqueara51@gmail.com | GDBJYZDB6YP6YE6G7DHWFJ4DPXJGCJAJJNFF5DCG3LWUZVYU7T42IWQJ | Yes |
| 5 | Md Sadique | sadiqueara51@gmail.com | GBLIIZTSQVGHMU64U3JZHKAZ7DR26SVLHQJ5GR6DI435IHTOR23KVJBG | Yes |
| 6 | Ansh Barnwal | anshbarnwal0712@gmail.com | GDBJNIQL4BEEGGFVZ2S5PNCA5K5SDNJ4MAAES2RSNIB5PK6ZUPVAS6CJ | Yes |
| 7 | Yash Keshri | keshriiyashh31@gmail.com | GAKBXA6UG52M7W55Z2ZLLAQRTLL6NL5BU4NRN2CQRIW3MAUGOV5Z6H6J | Yes |
| 8 | Keshav Kumar | thakurkeshav3210@gmail.com | GDRDS625DDZAGSIMNV6SYA5FDWAWHYJMHWUVTBYE4UB2UPPT22RWR463 | Yes |
| 9 | Nikhil Raj | nikhil595bro@gmail.com | GDC24A3YLRHHWI3TJOA4U32OWMDYXRWODOVXSRQT4KEVEESG7VDUTY7H | Yes |
| 10 | Pushkar Srivastava | pushkarsri0902@gmail.com | GBYVDOKQTTOYT7Q4Z4XSSE5ZUOPNQJYMJL2NBY5MHLWA6SVVOASIBAVV | Yes |

## 🔧 Feedback Implementation

| # | Feedback (from user) | Submitted By | Status | Implementation Notes |
|---|------------------------|---------------|--------|------------------------|
| 1 | Include real-time claim status updates with notifications | Ayush Rai | ✅ Done | Implemented via `react-hot-toast` with 15-second polling |
| 2 | Buttons are small | Roshan Gupta | ✅ Done | Increased button size/padding for better usability |
| 3 | Loading takes time | Md Sadique | ✅ Done | Optimized data fetching using `Promise.all` for parallel loading |
| 4 | Claim history should be downloadable | Ansh Barnwal | ✅ Done | Added downloadable claim history feature |
| 5 | Wallet connection needs guidance | Yash Keshri | ✅ Done | Added on-screen wallet connection guidance/instructions |
| 6 | Claim approval process should prevent users from approving their own claims | Keshav Kumar | ✅ Done | Added self-vote check to prevent voting on own claims |
| 7 | Error messages are too technical and difficult to understand | Nikhil Raj | ✅ Done | Simplified error messages for end users |
| 8 | Claims should require multiple votes before being approved or rejected | Pushkar Srivastava | ✅ Done | Implemented 3-vote quorum requirement |
| 9 | No suggestions | Mandavi Kumari | — | No action needed |

## 📈 Improvement Summary

Based on direct feedback from 10 onboarded testnet users, ClaimChain went through a focused round of improvements:

- **Trust & Fairness:** Added a self-vote check and a 3-vote quorum requirement so no single user can approve their own claim or push through a decision alone.
- **Usability:** Increased button sizes, simplified technical error messages, and added wallet connection guidance to make the app easier to use for first-time testers.
- **Performance:** Sped up data loading using `Promise.all` for parallel API calls, reducing wait times across the app.
- **Transparency:** Added real-time claim status notifications (via `react-hot-toast` with 15-second polling) and a downloadable claim history feature, giving users better visibility into their claims.

All 8 actionable feedback items from testers have been implemented and deployed to the live app.
