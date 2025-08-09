# Cardano Token Risk Analysis Bot (Telegram)

A Telegram bot for quick due diligence on **Cardano native tokens**: tokenomics, holder concentration, DEX liquidity, minting policy status, and a **transparent risk score** with explanations.  
**Open source (MIT)** · **Self-hosted** · **Read-only** (no keys, on-chain data only)

## Features
- Input `policy ID` / `asset ID` → get:
  - Supply & **minting policy lock/unlock** status
  - Holder distribution: top 1/5/10, concentration heuristics
  - Basic DEX liquidity info (if available)
  - Recent on-chain activity (mint/burn/large transfers)
  - **Risk score** (Low/Medium/High or 0–100) with rationale
- Friendly Telegram commands: `/scan`, `/score`, `/holders`, `/liquidity`, `/help`
- Modular architecture for new rules/data sources
- Choose your data source: self-hosted node/db-sync, or Blockfrost/Koios

## Quick demo (commands)
/scan <policy_or_asset_id>
/score <policy_or_asset_id>
/holders <policy_or_asset_id>
/liquidity <policy_or_asset_id>
/help

## Quick start
> Requirements: Node.js 18+, npm, and a Cardano data source (self-host `cardano-node + db-sync`/Ogmios, or use Blockfrost/Koios).

```bash
git clone https://github.com/<your-org>/<your-repo>.git
cd <your-repo>
cp .env.example .env
npm install
npm run dev
