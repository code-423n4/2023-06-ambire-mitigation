# Ambire Wallet - Mitigation Review details
- Total Prize Pool: $6,500 USDC 
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-C4-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Submit findings [using the C4 form](https://code4rena.com/contests/2023-06-ambire-wallet-mitigation-review/submit)
- Starts June 16,2023 20:00 UTC 
- Ends June 21, 2023 20:00 UTC 

## Important note 

Each warden must submit a mitigation review for *every High and Medium finding* from the parent audit. **Incomplete mitigation reviews will not be eligible for awards.**

## Findings being mitigated

Mitigations of all High and Medium issues will be considered in-scope and listed here.

- [M-01: Fallback handlers can trick users into calling functions of the AmbireAccount contract](https://github.com/code-423n4/2023-05-ambire-findings/issues/21)
- [M-02: Attacker can force the failure of transactions that use tryCatch](https://github.com/code-423n4/2023-05-ambire-findings/issues/18)
- [M-03: Recovery transaction can be replayed after a cancellation](https://github.com/code-423n4/2023-05-ambire-findings/issues/16)
- [M-04: Project may fail to be deployed to chains not compatible with Shanghai hardfork](https://github.com/code-423n4/2023-05-ambire-findings/issues/12)
- [M-05: AmbireAccount implementation can be destroyed by privileges](https://github.com/code-423n4/2023-05-ambire-findings/issues/10)

## Overview of changes

We fixed 3 of the vulmnerabilities after they were found, and we chose not to mitigate one.

## Mitigations to be reviewed

[ ⭐️ SPONSORS: PLEASE ADD A LINK TO THE BRANCH IN YOUR REPO CONTAINING ALL PRS ]

Wherever possible, mitigations should be provided in separate pull requests, one per issue. If that is not possible (e.g. because several audit findings stem from the same core problem), then please link the PR to all relevant issues in your findings repo. 

| URL | Mitigation of | Purpose | 
| ----------- | ------------- | ----------- |
| [fca50cd45478ef1ab57ba21bf7e1ccd15b310a05](https://github.com/AmbireTech/ambire-common/commit/fca50cd45478ef1ab57ba21bf7e1ccd15b310a05) | M-02 | Check gasleft to prevent this attack | 
| [1c0b06fbbbdd9aac1285d4fc4949f5b84f923238](https://github.com/AmbireTech/ambire-common/commit/1c0b06fbbbdd9aac1285d4fc4949f5b84f923238) | M-03 | Increment the nonce to prevent replaying recovery transactions | 
| [cf9c8b115a60df384ae8986a368bb65c56cd7e12](https://github.com/AmbireTech/ambire-common/commit/cf9c8b115a60df384ae8986a368bb65c56cd7e12) | M-04 | Downgrade Solidity to allow deploying on pre-Shanghai networks | 
| [3a0a4d9b24c96d816fb5819efe1e5f4dc57d7835](https://github.com/AmbireTech/ambire-common/commit/3a0a4d9b24c96d816fb5819efe1e5f4dc57d7835) | M-05 | To mitigate this and avoid confusion, we removed the constructor as it's not used anyway | 


## Out of Scope

### M-01: Fallback handlers can trick users into calling functions of the AmbireAccount contract
This is worth pointing out but the likelihood of an attack is very low, it needs the user to consciously add a malicious fallback handler and the UI needs to be updated to attack the user as well. If we go into the possibility of malicious UI updates, then we open a whole new can of worms which is completely out of scope - in other words, we will have much bigger issues in this case, so this is completely irrelevant.

Furthermore there's no applicable mitigation
