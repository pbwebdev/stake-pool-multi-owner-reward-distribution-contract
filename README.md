# Multi Owner Stake Pool Rewards Distribution Smart Contract

## Problem
With the price of ADA above $1 USD and with more people wanting to set up stake pools, the barrier to entry is a lot more difficult since it requires a large amount of stake to be able to mint blocks. With possible changes to the a0 parameter for rewards, a high pledge may be needed and become more beneficial to stake pool operators.

As a result, it would be more beneficial for multiple stake pool operators or user thinking about creating a pool to potentially combine their ADA into a single pool for an increased pledge.

For users that aren't aware, when registering a pool, the process allows for the creation of multiple owner wallets and a separate rewards address which combine to form the pledge.

There are so many pools at the moment with very few delegators, less than 10,000 pledge and almost no hope in creating a block without marketing or financial help. On the other hand, the huge increase of relay nodes for the Cardano network works in its favour with more peers, connections and decentralisation.

This doesn't solve the problem at the top end where large pool operators are creating multiple large pools that are close to or even oversaturated but will help to address the problem at the bottom end where ADA concentration is so thinly spread.

## Solution
A smart contract can calculate and distribute the amount of rewards to the pool owners based on their percentage level of contribution to the pools pledge. The minimum fixed fee (340 ADA) would go to the main operator of the pool that manages the hardware while the rest of the variable reward is divided up based on the percentage ownership of the pledge.

For example:

Owner 1: 10,000 ADA (Main Operator)
Owner 2: 50,000 ADA
Owner 3: 20,000 ADA
Owner 4: 20,000 ADA
Total ADA in pledge: 100,000

Owner 1 has a 10% share of the pool, owner 2 50%, owner 3 20% and owner 4 has 20%.

If a pool produces a block, and their variable fee is 1% and their fixed fee is 340 ADA, they may receive 1340 ADA.

Based on their percentage stake in the pool, when the 1,000 ADA is sent to the pools rewards wallet, it is divided 
up accordingly and sent to the corresponding wallets of the owners. This could be the wallet that is set on the pools pledge or a secondary wallet which the have access to.

Owner 1 would receive the 340 ADA as the fixed fee and 100 ADA.
Owner 2 would receive 500 ADA
Owners 3 and 4 would both receive 200 ADA.

This distribution is only of the variable fee portion of the pools fees. The standard delegation rewards still applies.

A percentage ownership variable could also apply to the main owner of the stake pool where the main owner would automatically own 50% of the pools variable reward and the remaining owners would have their rewards distributed based on percentage ownership of what is left. This would particularly benefit setups where others are simply silent partners in the pool and not participating in active marketing, community engagement or other Cardano related activities.

Overall, this can give multi pool owner stake more of an incentive to combine ADA to form a pledge as it increases their return on ADA.

The downside to this is that the ADA is locked into the pool and would be at the sole discretion of the stake pool operators to handle keys and access. It can lead to run away scams if not handled correctly.