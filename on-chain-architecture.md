# On-Chain Architecture

## Overview

| Component | Details |
|---|---|
| Blockchain | Base Mainnet (Chain ID: 8453) |
| Token | $GEM — ERC-20 at `0xD3776969966B340d72d75731eF890A3Bc9F21bA3` |
| Wallet | Coinbase Smart Wallet / Base App |
| Frontend | Vercel — auto-deploys on merge to main |
| Multiplayer | Cloudflare Workers (Durable Objects) |
| Database | Turso (libSQL) |

## Smart Contracts

### ForgeUpgrade
Handles pickaxe, armor, and stamina upgrades. Flow:
1. Player approves $GEM spend for the upgrade cost
2. Backend signer calls `upgrade(playerWallet, upgradeType, tier, gemAmount)`
3. Contract pulls $GEM via `transferFrom` and records the upgrade on-chain

### BurnGateNFT
Handles burn mechanics. Supports two paths:
- **Path A:** ERC-2612 permit signature (off-chain) + contract call
- **Path B:** Standard `approve` + transfer

## Wallet Connection

The game connects via the Base App wallet / Coinbase Smart Wallet. All transactions are on Base mainnet — gas fees are minimal.

## Security

- Contracts are verified on Basescan
- Approval amounts are exact (not unlimited)
- Registered with Blockaid for transaction simulation safety
