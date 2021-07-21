# Testing Results

At this time we chose to keep the smart contract build & test cases private. You can find results of our unit tests below:

```
  WATER Tests
    ✓ ensure proper construction parameters with 25m premine (112ms)
    ✓ ensure proper premine (59ms)
    ✓ ensure supply burns properly (146ms)

  WOOD Minting Tests
    ✓ ensure 1 WATER mints 0.00000001 WOOD per block (535ms)
    ✓ ensure minting produces expected amount of WOOD after calling it (364ms)
    ✓ ensure burn multiplier increases and decreases correctly (481ms)
    ✓ ensure burn multiplier increases and decreases correctly (155ms)
    ✓ ensure time reward at 2x and 3x is applied correctly (1158ms)

  WOOD Token Tests
    ✓ ensure proper construction parameters with 0 premined coins (39ms)
    ✓ ensure WOOD token can be operator of WATER account holder (78ms)
    ✓ ensure WATER holder can lock WATER in WOOD smart contract (106ms)
    ✓ ensure after locking-in WATER into WOOD you can unlock 100% of WATER back (337ms)
    ✓ ensure failsafe works (417ms)
    ✓ ensure WOOD can be minted after WATER lock-in to another address (318ms)
    ✓ ensure WOOD can be target-burned (300ms)


  15 passing (7s)
```
  
# Bsc Testnet Testing period

Before Mainnet launch we've undergone a number of deployments & testing stages. Thanks to our community for participating in testing where we've had a chance to test failsafe mode and our decentralized dashboard.

You can find examples of Bsc Testnet deployments here:
  
Waterwood (WATER) Token: https://testnet.bscscan.com/address/0x5bd45dc4107f0a915056448ad7cb40b955f1cade

WOOD Token: https://testnet.bscscan.com/address/0x9e940ee71a6AC0d70B2dEaa9383229523dC09F76
