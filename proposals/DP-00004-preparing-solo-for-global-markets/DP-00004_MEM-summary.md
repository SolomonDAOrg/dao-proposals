# DP-00004 (MEM): Preparing SOLO for Global Markets - Summary

**Status:** Draft (proposal memorandum; to be voted)

**Version:** 1.0.0

**NON-BINDING SUMMARY.** This memorandum is informational only and is subordinate to the governing
instruments and any adopted resolutions. In the event of conflict, the normative resolution text
controls.

---

## Summary

Solomon is entering public USDv launch alongside a significant expansion in product activity,
partnerships, distribution, and market reach. SOLO's futarchy AMM already contains approximately
$3 million of liquidity, making it the deepest market in the MetaDAO ecosystem, including META
itself. The Meteora pool has completed its original role as an indexed discovery venue.

This proposal withdraws the DAO's entire single-sided Meteora position and returns approximately
900,000 SOLO to the Company Treasury Vault. With substantial liquidity already available through
the futarchy AMM, removing the legacy position will allow SOLO to respond more directly to new
demand as the launch unfolds. The returned assets can later support broader exchange access,
professional market-making arrangements, ecosystem rewards, and Solomon's continued expansion,
subject to separate governance approval.

---

## Rationale

The Meteora SOLO-USDC pool was established during SOLO's initial phase as a discovery venue.
Although the futarchy AMMs had sufficient liquidity, they were not indexed by Dexscreener and other
widely used market-data platforms. The Meteora pool ensured that SOLO could be found, tracked, and
accessed through conventional market interfaces.

That bootstrap function has now been served. Futarchy AMMs have since gained the visibility required
to support the market directly. SOLO's futarchy AMM currently contains
[approximately $3 million of liquidity](https://solscan.io/account/DzYtzoNvPbyFCzwZA6cSm9eDEEmxEB9f8AGkJXUXgnSA),
giving it the largest liquidity base of any project in the MetaDAO ecosystem, including META itself.
That depth is sufficient to support active trading independently of the Meteora position.

Meanwhile, the Meteora position leaves approximately 900,000 treasury-owned SOLO in a single-sided
position that mechanically supplies inventory as demand increases. The position was useful when
conventional market visibility was the priority. With that constraint resolved, it now fragments
trading across venues and limits how directly the market can respond to new demand.

That structure is poorly matched to Solomon's next phase. The public launch is expected to bring new
product activity, partnerships, distribution, and broader market attention. Removing the legacy
position will concentrate trading within an already deep futarchy AMM and allow organic supply and
demand to absorb new information without a large treasury position continuously leaning against
incremental demand.

Withdrawal will also return strategically useful SOLO to the Company Treasury Vault. Subject to
later governance approval, those assets may support broader exchange access, professional
market-making arrangements, new trading venues, ecosystem rewards, and other initiatives connected
to Solomon's launch and growth.

This proposal authorizes only the withdrawal and transfer of the assets. Any subsequent deployment
will require separate governance approval.

---

## Key Parameters

- **Pool:** Meteora DAMM v2 SOLO-USDC
- **Pool Address:** `2zsbECzM7roqnDcuv2TNGpfv5PAnuqGmMo5YPtqmUz5p`
- **Network:** Solana mainnet-beta
- **Withdrawal Amount:** `100% of the DAO's liquidity position`
- **Approximate Current Position:** `900,017.47 SOLO`, presently single-sided and subject to change
  through ordinary pool activity
- **Assets to Be Received:** All SOLO and USDC attributable to the DAO's liquidity position at
  execution
- **Destination:** Company Treasury Vault at
  `8GVq1srBAZBsCeYpwdKUwEXzDffwAE5xSLWB1ec2gerr`
- **SOLO Mint:** `SoLo9oxzLDpcq1dpqAgMwgce5WqkRDtNXK7EPnbmeta`
- **USDC Mint:** `EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v`
- **Execution Method:** Standard Meteora DAMM v2 withdrawal instructions followed by transfer to the
  Company Treasury Vault
- **Future Use:** Potential broader exchange access, professional market-making arrangements, new
  trading venues, ecosystem rewards, and other strategic initiatives, subject in every case to
  separate governance approval

## Process

If this proposal is adopted, the Governance System will authorize the Treasury Executor to unwind
the DAO's entire liquidity position in the Pool.

The Execution Bundle will:

1. withdraw 100% of the DAO's position from the Pool, subject only to de minimis residual dust that
   cannot be economically withdrawn;
2. receive all SOLO and USDC attributable to that position at the time of execution; and
3. transfer the Withdrawn Assets promptly to the Company Treasury Vault.

The assets will then remain in the Company Treasury Vault until a later governance proposal
authorizes a specific use.

---

## Section 1. Authorization of Pool Withdrawal

Resolved, that the DAO hereby authorizes the Treasury Executor to withdraw 100% of the DAO's
liquidity position from the Pool.

Resolved further, that this authority applies only to the Meteora DAMM v2 SOLO-USDC pool at
`2zsbECzM7roqnDcuv2TNGpfv5PAnuqGmMo5YPtqmUz5p`.

---

## Section 2. Assets Covered and Treasury Transfer

Resolved, that all SOLO and USDC received from withdrawing the DAO's position shall be treated as
Withdrawn Assets under this proposal.

Resolved further, that if the position contains both SOLO and USDC at the time of execution, the
Treasury Executor shall withdraw both assets in full. No separate governance action is required
merely because ordinary pool activity changes the composition of the position between proposal
publication and execution.

Resolved further, that the Execution Bundle shall transfer all Withdrawn Assets promptly to the
Company Treasury Vault at `8GVq1srBAZBsCeYpwdKUwEXzDffwAE5xSLWB1ec2gerr`.

---

## Section 3. No Current Deployment Authority

Resolved, that this proposal does not authorize any person or body to distribute, commit, allocate,
sell, swap, transfer, lend, stake, pledge, use as collateral, use as market-making inventory, or
otherwise deploy the Withdrawn Assets after they reach the Company Treasury Vault.

Until later governance action authorizes a specific use, the Withdrawn Assets shall remain held in
the Company Treasury Vault.

---

## Section 4. Core Guardrails

The Treasury Executor must implement this proposal subject to the following constraints:

- the DAO's entire Meteora DAMMv2 liquidity position must be withdrawn
- no borrowing, margin, leverage, or derivatives may be used;
- no swap or trade is authorized as part of execution;
- the Withdrawn Assets may not be used between withdrawal and transfer to the Company Treasury
  Vault;
- no wash trading or transaction intended to mislead market participants is permitted; and
- no other liquidity pool, vault, staking position, or DAO-controlled asset may be withdrawn from or
  otherwise affected.

---

## Section 5. Residual Dust and Execution Record

If a residual balance remains because of rounding, minimum withdrawal thresholds, or another
technical limitation that makes withdrawal economically impractical, the residual will not
constitute a failure to execute this proposal.

The governance record shall disclose:

- the execution transaction signature or signatures;
- the actual amount of SOLO withdrawn and transferred;
- the actual amount of USDC withdrawn and transferred, if any; and
- any residual dust left in the Pool or the DAO's liquidity position.

---

## Plain English

If adopted, this proposal means:

- the Meteora position has completed its original token-discovery purpose;
- the DAO exits its entire position in one specifically identified Meteora SOLO-USDC pool as Solomon
  enters its public launch phase;
- all SOLO and USDC received from that exit go to the Company Treasury Vault;
- trading and price formation become more concentrated within the indexed futarchy AMMs;
- the proposal does not touch any other DAO position or asset; and
- the withdrawn assets stay in the treasury until governance separately approves their use,
  including any future exchange access, professional market making, new trading venue, rewards
  program, or other strategic initiative.

---

## Links

- Full normative resolution text (controls if there is any conflict with this summary):
  [DP-00004_MEM-full.md](https://github.com/SolomonDAOrg/dao-proposals/blob/main/proposals/DP-00004-preparing-solo-for-global-markets/DP-00004_MEM-full.md)

- Compiled proposal PDF:
  [DP-00004_preparing-solo-for-global-markets.pdf](https://github.com/SolomonDAOrg/dao-proposals/blob/main/proposals/DP-00004-preparing-solo-for-global-markets/DP-00004_preparing-solo-for-global-markets.pdf)

- Proposal repository (canonical history + execution artefacts):
  [https://github.com/SolomonDAOrg/dao-proposals](https://github.com/SolomonDAOrg/dao-proposals)

---

**Disclaimer (Governance Proposal; No Professional Advice).**

This document is a governance proposal and governance communication. If adopted by the DAO through
its governance mechanisms, it may become binding on the DAO and persons exercising authority under
the Company Agreement to the extent provided in the Company Agreement and applicable law. This
document does not constitute legal, tax, financial, or other professional advice. The author(s) are
not acting as legal counsel to the DAO or any member or user. No attorney-client relationship is
created.

You must obtain your own independent advice for your circumstances.
