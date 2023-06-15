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

[ ⭐️ SPONSORS ADD INFO HERE ]

## Overview of changes

Please provide context about the mitigations that were applied if applicable and identify any areas of specific concern.

## Mitigations to be reviewed

[ ⭐️ SPONSORS: PLEASE ADD A LINK TO THE BRANCH IN YOUR REPO CONTAINING ALL PRS ]

Wherever possible, mitigations should be provided in separate pull requests, one per issue. If that is not possible (e.g. because several audit findings stem from the same core problem), then please link the PR to all relevant issues in your findings repo. 

| URL | Mitigation of | Purpose | 
| ----------- | ------------- | ----------- |
| https://github.com/code4rena/sample-contracts/pull/XXX | H-01 | This mitigation does XYZ | 

## Out of Scope

Please list any High and Medium issues that were judged as valid but you have chosen not to fix.
