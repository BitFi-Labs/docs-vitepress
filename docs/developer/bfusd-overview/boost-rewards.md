---
title: Boost Rewards
---

# Boost Rewards Program

Boost Rewards uses Horizon’s insurance premium to top up Pulsar allocations and favor holders who demonstrate episode-long discipline with their Pulsar bfUSD positions.

> **TL;DR:** The longer you hold Pulsar bfUSD without shrinking your position, the higher your continuity score, the greater your weight per snapshot, and the more Boost Rewards you collect each cycle.

## What is Boost Rewards?

Boost Rewards is an additional subsidy paid to Pulsar users. Instead of distributing the insurance premium solely by balance, the mechanism also factors in how consistently and stably a holder maintains their position. This design amplifies rewards for long-term, steady participants.

## Distribution goals and principles

- **Goal**: Share Horizon’s insurance premium with Pulsar users, prioritizing those who keep funds in the pool for longer stretches.
- **Principle**: Reward allocation is shaped by both size and behavior—frequent reductions shrink your continuity score and lower future weights.

## Periods and snapshots

Each Boost period (currently ~30 days) samples user balances at fixed intervals (e.g., every 6 hours). Every snapshot calculates an instantaneous weight, and the period’s average weight determines the reward share.

## Calculating user weight

Each snapshot weight blends two components:

- **Held amount** $S_k$: Your Pulsar bfUSD balance at snapshot $k$.
- **Continuity multiplier** $M(C_k)$: Derived from the continuity score $C_k$.

### 1. Snapshot weight

$$
W_k = S_k \times M(C_k)
$$

### 2. Continuity multiplier (exponential curve)

$$
M(C) = \text{Base}^{\frac{C - 1}{N_{total}}}
$$

- $\text{Base}$ controls how steeply rewards favor high $C$ (larger Base accentuates long-term holding).
- $N_{total}$ is the total number of snapshots in the period.
- $C$ is the continuity score, reflecting how stable your holding has been.

### 3. Period average weight

$$
W_{avg} = \frac{1}{N_{total}} \sum_{k=1}^{N_{total}} W_k
$$

### 4. Reward allocation

When the period closes and the reward pool $R_{total}$ is finalized, each user receives:

$$
R_{user} = R_{total} \times \frac{W_{avg,user}}{\sum W_{avg,all}}
$$

> You do not need to know how $R_{total}$ is generated—Horizon aggregates the insurance premium and uses it to fund Boost Rewards in each settlement.

## Updating continuity score $C$

1. **Start**: The first snapshot with a non-zero position initializes $C$ at 1.
2. **Grow**: If the current snapshot balance $S_{new} \geq S_{old}$, increment $C$ by 1.

   $$
   C_{new} = C_{old} + 1
   $$

3. **Adjust**: If the balance drops ($S_{new} < S_{old}$), scale $C$ down proportionally and round up:

   $$
   C_{new} = \left\lceil C_{old} \times \frac{S_{new}}{S_{old}} \right\rceil
   $$

   This penalizes sudden withdrawals—larger reductions cause sharper drops in $C$, and as a result, your multiplier and future weights decline.

4. **Reset**: When your balance hits zero, the continuity score stops counting. A new position restarts $C$ from 1.

## Claiming rewards (bfUSD → pbfUSD)

Boost Rewards are denominated in bfUSD but paid out as Pulsar bfUSD (pbfUSD) at the time of claim. The amount of pbfUSD you receive depends on the prevailing share price (ratio) of pbfUSD in bfUSD:

$$
\text{pbfUSD}_{received} = \frac{\text{bfUSD}_{reward}}{\text{Price}_{\text{pbfUSD in bfUSD}}}
$$

## Timing and target APY

- **Distribution cadence**: Each Boost period is roughly 30 days; rewards are settled and delivered once every cycle, subject to official notices and on-chain execution.
- **Target APY**: Determined by Horizon’s earnings and the size of the insurance premium; it depending on how much Horizon earns and how much capital sits in the Pulsar pool.

## What it means for you

- To maximize Boost Rewards, keep a consistent Pulsar bfUSD balance and avoid large withdrawals.
- Adding more to your position does not reset $C$, but reducing it does—so weight and rewards decrease when you shrink your balance.
