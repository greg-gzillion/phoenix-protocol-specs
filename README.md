# phoenix-protocol-specs
P2P auction protocol for physical precious metals, built with CosmWasm smart contracts on Coreum and settled with XRP.


# Phoenix Protocol: Sovereign Precious Metals Exchange

## The Problem
*   COMEX/LBMA paper price manipulation.
*   eBay/Dealer fees (15%) and reversible chargebacks.
*   Illiquidity and unfair pricing for physical holders 

## The Solution: A Peer-to-Peer Auction Protocol
A decentralized, non-custodial marketplace where:
1.  **Sellers** list tokenized physical assets with a reserve price and a bond.
2.  **Buyers** bid in XRP (or other XRPL assets, auto-swapped to XRP).
3.  **Smart Contracts** (CosmWasm on Coreum) atomically swap the asset for funds upon a successful auction.
4.  **Immutable On-Chain Feedback** creates permanent, transparent reputation.

## Core Technical Architecture
*   **Blockchain**: Coreum (for RWA tokenization and smart contracts).
*   **Smart Contracts**: CosmWasm (for the bonded auction escrow logic).
*   **Settlement**: XRP (as the base settlement currency).
*   **Key Mechanism**: Bonded escrow with automatic penalties for failed shipping, time-locked finalization, and decentralized dispute resolution.

## Incentive & Trust Model
*   **Seller Bond**: Slashed for failing to ship, compensating the buyer.
*   **Finality**: Sales are final after a 48-hour inspection window; funds release automatically.
*   **Reputation**: A single, immutable rating (1-5) is stored on-chain per transaction, linked to wallet addresses.

## Getting Started (For Developers)
This repository contains the protocol specifications. The next phase is building the core CosmWasm auction contract.

## License
This project is licensed under the GNU General Public License v3.0 - see the LICENSE file for details.
