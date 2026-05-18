---
title: Public Sale Details
---

# Public Sale Details

The BitFi Public Sale is conducted through Sonar, Echo's public sale infrastructure for identity verification, eligibility checks, and compliant on-chain participation.

## Overview

BitFi is opening access to BFI, the native token of the BitFi ecosystem, for users, supporters, and long-term participants who believe in institutional-grade on-chain asset management for Bitcoin and stablecoins.

BFI is designed to support BitFi's long-term growth through governance, staking-based utility, ecosystem incentives, liquidity pairing, and broader participation across the network. The Public Sale is intended to widen access beyond early backers while keeping the sale structure clear, fixed-price, and pro-rata.

## Sale Facts

| Item | Details |
| --- | --- |
| Token | BFI |
| Maximum Supply | 1,000,000,000 BFI |
| Public Sale Supply | 10,000,000 BFI, equal to 1.00% of total supply |
| Standard Sale Price | $0.05 per BFI |
| Implied FDV | $50,000,000 |
| Target Raise | $500,000 |
| Pricing Model | Fixed Price |
| Settlement Model | Pro-Rata |
| Accepted Assets | USDC / USDT on Ethereum |
| Supported Chain | Ethereum |
| Token Standard | ERC-20 |
| Crosschain Standard | LayerZero OFT |
| Day-1 Float | 14.50%, or 145,000,000 BFI |

If the sale is oversubscribed, each participant's contribution is scaled down proportionally so that total allocations match the available supply. Any unfilled commitment amount is refunded or made claimable according to the final sale rules.

## Participation Tracks

| Track | Eligibility | Price | Unlock |
| --- | --- | --- | --- |
| Track A: Standard | Non-U.S. participants, subject to eligibility and jurisdiction rules | $0.05 per BFI | 100% unlocked at TGE |
| Track B: Locked | Mandatory for verified U.S. accredited investors; optional for eligible non-U.S. participants | $0.045 per BFI, equal to a 10% discount | 12-month lock-up from TGE |

Locked tokens cannot be transferred or sold during the lock-up period and do not earn staking rewards while locked.

## U.S. Participant Lock-Up Requirement

U.S. participants, if eligible to participate, must complete Sonar's required identity, residency, and accreditation checks and must use the locked participation track.

BFI allocated to U.S. participants is subject to a mandatory 12-month lock-up from TGE. During the lock-up period, these tokens cannot be transferred, sold, or staked, and they do not earn staking rewards while locked.

Sonar supports this requirement through its U.S. investor forced-lockup configuration. When a participant is identified as a U.S. entity, the sale flow must submit the commitment with the lock-up flag enabled; otherwise, the sale contract may reject the commitment.

## Why This Sale

BitFi is not launching BFI as a standalone token event. The Public Sale is part of the next phase of the BitFi ecosystem, aligning users, contributors, and long-term stakeholders around protocol growth.

The sale price is fixed in alignment with the seed round valuation. The intention is for public sale participants to enter at the same valuation as the earliest strategic supporters of the project, rather than at a premium.

## How It Works

1. **Get Started**  
   Begin the application through Sonar by creating an account and starting the onboarding process.

2. **Verify Eligibility**  
   Complete identity, residency, and eligibility checks through Sonar. Participation remains subject to jurisdictional requirements, accreditation requirements where applicable, sanctions screening, and wallet risk screening.

3. **Connect Wallet**  
   Link the Web3 wallet you will use for the Public Sale. The wallet must be associated with the verified Sonar entity before it can submit a commitment.

4. **Run Pre-Purchase Checks**  
   Before a commitment is submitted, the sale flow checks whether the entity is eligible, the wallet is linked and approved, the sale is active, the transaction is inside the sale window, and the amount is within the configured limits.

5. **Generate Purchase Permit**  
   Sonar generates a short-lived signed purchase permit for the eligible entity and linked wallet. The permit is passed to the sale contract together with the purchase transaction.

6. **Submit Commitment**  
   Submit an on-chain commitment during the live sale window using the accepted assets and network specified above. The sale contract verifies the Sonar permit before accepting the commitment.

7. **Settlement and Refunds**  
   After the sale closes, final allocations are calculated. If the sale is oversubscribed, commitments may be scaled according to the final allocation logic.

   Any unallocated commitment amount is refunded or made claimable according to the final sale rules.

8. **Receive BFI at TGE**  
   BFI purchased in the Public Sale is expected to be distributed at TGE. Standard-track tokens are fully unlocked at distribution; locked-track tokens follow the applicable lock-up terms.

## Timeline

| Event | Timing |
| --- | --- |
| Registration Opens | To be announced |
| Sale Window | To be announced |
| Settlement | After sale close |
| Refunds / Claims | Available after settlement, according to final sale rules |
| TGE | To be announced |
| Token Distribution | Public Sale tokens distributed at TGE |

## Allocation, Refund, and Claim

Public Sale tokens represent 1.00% of the total BFI supply. Final allocation depends on the total eligible commitments received during the sale.

If the sale is oversubscribed, allocations are distributed pro-rata. For example, if the sale is 2x oversubscribed, each participant receives 50% of the committed amount as allocation and the remaining 50% is refunded or made claimable according to the sale rules.

If the sale is undersubscribed, the sale may still proceed according to the final terms. Any unsold allocation will be handled according to BitFi's broader token distribution framework.

## Disclaimer

This page is for informational purposes only. It does not constitute investment, legal, tax, or financial advice, and it is not an offer or solicitation to buy or sell securities or financial instruments.

Digital assets involve significant risk, including the risk of total loss. Participation in the Public Sale is subject to eligibility checks, KYC, sanctions screening, jurisdictional restrictions, and the final sale terms.
