# Waterwood WOOD Economic Model - Breakdown of Smart Contracts

## Precursor

Here we will describe the inner workings of the smart contract and lay it out on a step-by-step basis. This page does not describe WHY our economic system works but HOW it works behind the scenes. This page is not going to include various security and exception checks in place to ensure there is even and fair distribtuion of WOOD.

## Assumptions

- Block = 3 seconds = 1 Bsc Block (the whole ecosystem adjusts as block times change)

## Ecosystem Rules

### WATER Lock-in

#### When WATER tokens are locked-in the following is true:

- Your Waterwood (WATER) tokens are sent to the smart contract and WATER balance is subtracted from your address
- Your total burned WOOD is ADDED to the global burned WOOD pool
- Your total WATER lock-in is ADDED to the global locked-in WATER pool

#### When WATER tokens are unlocked the following is true:

- Your Waterwood (WATER) tokens are sent back from the smart contract and WATER balance is added to your address
- Your total burned WOOD is REMOVED from the global burned WOOD pool
- Your total WATER lock-in is REMOVED from the global locked-in WATER pool

#### When you mint WOOD the following is true:

- Your unminted amount is calculated (using the section below) and added to your address
- You can mint WOOD at any time on-demand as long as the unminted amount is >0
- Your unminted amount is reset to 0

## WOOD minting formula

**Unminted WOOD Amount** = (((0.00000001 * (WATER tokens Locked-in) * Unminted Blocks * Burn Bonus Multiplier ) / 10000) * Time bonus multiplier) / 10000

### Burn Bonus Multiplier

**My Ratio** = (My total burned WOOD for this address * 10000) / (My total locked-in WATER tokens)

**Global Ratio** = (Worldwide total burned WOOD for this address * 10000) / (Worldwide total locked-in WATER tokens)

**Bonus Multiplier** = Math.min(500000, ((MyRatio * 10000) / (Global Ratio)) + 10000)

### Time Bonus Multiplier

**Time Multiplier** = Math.min(100000, ((Unminted Amount * 90000) / 518400) + 10000)


## Burning WOOD

When you burn WOOD to a specific address the following happens:

- Address burned amount goes up by the amount burned
- Global burned pool amount goes up by the amount burned
