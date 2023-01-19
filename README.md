# Cooler Loans contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Resources

- [Docs](https://ag0.gitbook.io/cooler-loans/)
- [Walkthrough](https://ag0.gitbook.io/cooler-loan-code-walkthrough/)

# On-chain context

```
DEPLOYMENT: Mainnet
ERC20: Any
ERC721: None
ERC777: None
FEE-ON-TRANSFER: None
REBASING TOKENS: None
ADMIN: P2P + Restricted
```

In case of restricted, by default Sherlock does not consider direct protocol rug pulls as a valid issue unless the protocol clearly describes in detail the conditions for these restrictions. 
For contracts, owners, admins clearly distinguish the ones controlled by protocol vs user controlled. This helps watsons distinguish the risk factor. 
Example: 
* `ContractA.sol` is owned by the protocol. 
* `admin` in `ContractB` is restricted to changing properties in `functionA` and should not be able to liquidate assets or affect user withdrawals in any way. 
* `admin` in `ContractC` is user admin and is restricted to only `functionB`

# Audit scope

Cooler.sol & Factory.sol
ClearingHouse.sol

# About Cooler Loans

Cooler is a peer-to-peer lending protocol allowing a borrower and lender to engage in fixed-duration, fixed-interest lending. Cooler Loans are lightweight, trustless, independent of price-based liquidation, and allow borrowers to maintain delegation power over their committed collateral.
