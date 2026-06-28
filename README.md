contract address :
<img width="1883" height="881" alt="image" src="https://github.com/user-attachments/assets/8d96b807-8877-42b8-9b45-9bc0f4f5987e" />

UI Screenshot :
<img width="1895" height="901" alt="image" src="https://github.com/user-attachments/assets/79e73460-b285-46a7-b9d3-139dd0abd2b0" />


CI/CD pipeline badge : <img width="1862" height="630" alt="image" src="https://github.com/user-attachments/assets/cad7c3b9-a072-435a-b7f2-a6538275aee5" />


Live Demo Link : https://insurance-claims-syste-git-main-nishant-kumar-s-projects16.vercel.app


 mobile responsive view : 

 
 <img width="400" height="1568" alt="image" src="https://github.com/user-attachments/assets/4c8a71e4-9278-4eca-adb8-85a83968b3da" />





# ðŸ›¡ï¸ ClaimChain â€” Decentralized Insurance Claims System

## ðŸ“Œ Project Description  
Traditional insurance is plagued by centralized gatekeepers â€” adjusters, administrators, and executives who decide whether your claim gets paid, and when. ClaimChain eliminates all of that.  

Built on *Stellar Soroban*, ClaimChain is a decentralized application (DApp) where insurance claims are filed, reviewed, and paid out entirely on-chain through community consensus. There is no owner, no admin role, and no privileged address â€” the smart contract is permissionless by design.  

Claimants stake a small amount of XLM when filing, which deters spam. The broader community votes on claim validity. Once voting ends, anyone can trigger resolution and payout â€” the contract enforces the outcome automatically.  

---

## âš™ï¸ What It Does  
- Fund the insurance pool â€” anyone can contribute XLM  
- File a claim with title, description, evidence URI, and amount  
- Vote on claims (approve/reject) during a 3-day window  
- Resolve claims once voting ends and quorum is met  
- Execute payouts for approved claims  
- Reclaim 50% stake for rejected claims  

---

## âœ¨ Features  

### Core  
- ðŸ”“ Fully permissionless (no owner, no admin)  
- ðŸ—³ï¸ Community voting with quorum & threshold  
- âš¡ Trustless automatic payouts  
- ðŸ›¡ï¸ Stake-based spam deterrence  
- ðŸŽ Voter rewards (1% of claim)  
- ðŸ“Ž Evidence via IPFS/URLs  
- ðŸŒ Open funding pool  

### DApp Frontend  
- ðŸ¦Š Freighter wallet integration  
- ðŸ“Š Live on-chain data via Soroban RPC  
- ðŸ§¾ Explorer links (Stellar Expert)  
- ðŸŽ¨ Terminal-style UI (IBM Plex Mono)  
- ðŸ“± Responsive design  

### Contract Mechanics  
- Voting Period: 3 days  
- Minimum Quorum: 3 votes  
- Approval Threshold: 60%  
- Claimant Stake: 0.01 XLM  
- Max Claim Amount: 10,000 XLM  
- Voter Reward: 1% (split equally)  
- Rejected Stake Returned: 50%  

---

## ðŸ”„ How It Works  
1. User files a claim with 0.01 XLM stake  
2. 3-day voting window starts  
3. Community votes approve/reject  
4. After voting ends, anyone calls resolve_claim()  
5. If â‰¥60% approve â†’ payout executed  
6. If <60% approve â†’ 50% stake returned  

---

## ðŸ“œ Smart Contract  
 
- *Contract Address:*  
  CA43I2DUWKVEMKEFKNRNACVVKJYHN6SLJ6B6GACIV5SC3GUC6APWDSXN  

- *Freighter Address:*  
  GD3KADPLFNCKMGLTJS2AXUU3KWSSNJH3C3MA3OC3PGOAMAYC35S5SFWQ  

---

## ðŸ›  Tech Stack  
- Rust Â· Soroban SDK  
- Stellar Mainnet  
- Soroban RPC (soroban.stellar.org)  
- Vanilla JS Â· HTML Â· CSS  
- @stellar/stellar-sdk v12  
- Freighter Wallet  
- IPFS  
- Stellar Expert  

---

## ðŸš€ Getting Started  

### Prerequisites  
- Freighter wallet installed  
- Stellar Mainnet account with XLM  
- Modern browser  

### Run Locally  
git clone https://github.com/your-org/claimchain  
cd claimchain  
open ClaimChain_Stellar.html  

Or:  
npx serve .  

---

## ðŸ“ Contract Functions  

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

---

## ðŸ”“ Permissionless Design  
- No owner or admin roles  
- No whitelist system  
- Anyone can resolve claims  
- Anyone can execute payouts  
- Anyone can reclaim stake  
- Economic incentives replace moderation  
- Time-based rules enforced by smart contract


---

## ðŸ‘¥ User Feedback

We are onboarding testnet users to improve ClaimChain!

ðŸ‘‰ **Fill out our feedback form:** [ClaimChain User Feedback Form](https://docs.google.com/forms/d/e/1FAIpQLSc3kZlOxoRcCHYj-njzyPynmGXaL3dFjX2ytfSwXKXQkngW1w/viewform?usp=publish-editor)

### How to test ClaimChain:
1. Visit [insurance-claims-syste.vercel.app](https://insurance-claims-syste.vercel.app)
2. Connect your Stellar testnet wallet
3. File a claim or vote on existing claims
4. Fill out the feedback form above
