# DP-00004: Preparing SOLO for Global Markets

**Status:** Draft (intended for ratification via Governance System)

**Version:** 1.0.0

**Owner:** SOLOMON DAO LLC (via Governance System)

**Applies to:** DAO governance participants; the Treasury Executor; and any
person or body handling the Withdrawn Assets or the Company Treasury Vault.

**Effective date:** Upon ratification by Governance System and successful
on-chain execution of the Execution Bundle.

**Authority note:** This Resolution authorizes only withdrawal of the DAO's
liquidity position from the Pool and transfer of the Withdrawn Assets to the
Company Treasury Vault. It does not authorize any subsequent deployment of
the Withdrawn Assets.

**Confidentiality classification:** Public (operational/security-sensitive
details may be handled under appropriate confidentiality controls)

**Supersedes:** None

**Related:** None

---

## Intellectual Property Firewall

**"Protocol"** in this Resolution has the same meaning as **"Protocol IP"**
as defined in the Company Agreement of SOLOMON DAO LLC (Operating Agreement
Section 2.1(17)) -- design, documentation, code, repositories, and other
intellectual property. It does not mean an operating business, service,
issuer, custodian, counterparty, or other person or entity.

Nothing in this Resolution authorizes the Company, the Head Steward, or any
Subcommittee to direct, supervise, or control the operations of any Licensee,
counterparty, service provider, or other person. Any external obligations
arise only under the applicable License or other written agreement, and only
to the extent expressly stated there.

---

## 1. Purpose

This Resolution does two things:

1. Authorizes the Treasury Executor to withdraw 100% of the DAO's liquidity
   position from the Pool, subject only to de minimis residual dust that
   cannot be economically withdrawn.
2. Requires all SOLO and USDC received from the withdrawal to be transferred
   promptly to the Company Treasury Vault and held there until later
   governance action authorizes a specific use.

---

## 2. Operative rule

This is normative text proposed for adoption by Governance System. If (and
only if) it is adopted and the Execution Bundle executes successfully, the
operative clauses below are effective as stated.

---

## 3. Definitions

1. **"Company Treasury Vault"** means the treasury vault at
   `8GVq1srBAZBsCeYpwdKUwEXzDffwAE5xSLWB1ec2gerr`.

2. **"Execution Bundle"** means the on-chain instructions that implement the
   withdrawal and transfer authorized by this Resolution.

3. **"Governance System"** means the on-chain mechanism by which this
   Resolution is adopted and executed.

4. **"Pool"** means the Meteora DAMM v2 SOLO-USDC pool on Solana mainnet-beta
   at `2zsbECzM7roqnDcuv2TNGpfv5PAnuqGmMo5YPtqmUz5p`.

5. **"SOLO"** means the SOLO token (mint/address:
   `SoLo9oxzLDpcq1dpqAgMwgce5WqkRDtNXK7EPnbmeta`).

6. **"Treasury Executor"** means the person or body authorized through the
   Governance System to execute the withdrawal and transfer authorized by
   this Resolution.

7. **"USDC"** means the USDC token (mint/address:
   `EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v`).

8. **"Withdrawn Assets"** means all SOLO and USDC attributable to the DAO's
   liquidity position and received from withdrawal of that position at the
   time of execution.

---

## 4. Background and rationale

Solomon is entering public USDv launch alongside a significant expansion in
product activity, partnerships, distribution, and market reach. SOLO's
futarchy AMM already contains approximately $3 million of liquidity, making
it the deepest market in the MetaDAO ecosystem, including META itself. The
Meteora pool has completed its original role as an indexed discovery venue.

This Resolution withdraws the DAO's entire single-sided Meteora position and
returns approximately 900,000 SOLO to the Company Treasury Vault. With
substantial liquidity already available through the futarchy AMM, removing
the legacy position will allow SOLO to respond more directly to new demand as
the launch unfolds. The returned assets can later support broader exchange
access, professional market-making arrangements, ecosystem rewards, and
Solomon's continued expansion, subject to separate governance approval.

The Meteora SOLO-USDC pool was established during SOLO's initial phase as a
discovery venue. Although the futarchy AMMs had sufficient liquidity, they
were not indexed by Dexscreener and other widely used market-data platforms.
The Meteora pool ensured that SOLO could be found, tracked, and accessed
through conventional market interfaces.

That bootstrap function has now been served. Futarchy AMMs have since gained
the visibility required to support the market directly. SOLO's futarchy AMM
currently contains
[approximately $3 million of liquidity](https://solscan.io/account/DzYtzoNvPbyFCzwZA6cSm9eDEEmxEB9f8AGkJXUXgnSA),
giving it the largest liquidity base of any project in the MetaDAO ecosystem,
including META itself. That depth is sufficient to support active trading
independently of the Meteora position.

Meanwhile, the Meteora position leaves approximately 900,000 treasury-owned
SOLO in a single-sided position that mechanically supplies inventory as
demand increases. The position was useful when conventional market visibility
was the priority. With that constraint resolved, it now fragments trading
across venues and limits how directly the market can respond to new demand.

That structure is poorly matched to Solomon's next phase. The public launch is
expected to bring new product activity, partnerships, distribution, and
broader market attention. Removing the legacy position will concentrate
trading within an already deep futarchy AMM and allow organic supply and
demand to absorb new information without a large treasury position
continuously leaning against incremental demand.

Withdrawal will also return strategically useful SOLO to the Company Treasury
Vault. Subject to later governance approval, those assets may support broader
exchange access, professional market-making arrangements, new trading venues,
ecosystem rewards, and other initiatives connected to Solomon's launch and
growth.

This Resolution authorizes only the withdrawal and transfer of the assets. Any
subsequent deployment will require separate governance approval.

---

## 5. Pool withdrawal authorization

### 5.1 Authorization

**RESOLVED:** The DAO authorizes the Treasury Executor to withdraw 100% of the
DAO's liquidity position from the Pool.

### 5.2 Pool limitation

**RESOLVED:** This authority applies only to the Pool.

### 5.3 Current position

Informative note (non-binding): At drafting, the position is approximately
`900,017.47 SOLO`, presently single-sided and subject to change through
ordinary pool activity.

---

## 6. Assets covered and treasury transfer

### 6.1 Withdrawn Assets

**RESOLVED:** All SOLO and USDC received from withdrawing the DAO's position
shall be treated as Withdrawn Assets under this Resolution.

### 6.2 Position composition at execution

**RESOLVED:** If the position contains both SOLO and USDC at the time of
execution, the Treasury Executor shall withdraw both assets in full. No
separate governance action is required merely because ordinary pool activity
changes the composition of the position between proposal publication and
execution.

### 6.3 Transfer instruction

**RESOLVED:** The Execution Bundle shall transfer all Withdrawn Assets promptly
to the Company Treasury Vault.

Informative note (non-binding): The stated execution method is standard
Meteora DAMM v2 withdrawal instructions followed by transfer to the Company
Treasury Vault.

---

## 7. No current deployment authority

**RESOLVED:** This Resolution does not authorize any person or body to
distribute, commit, allocate, sell, swap, transfer, lend, stake, pledge, use
as collateral, use as market-making inventory, or otherwise deploy the
Withdrawn Assets after they reach the Company Treasury Vault.

**RESOLVED:** Until later governance action authorizes a specific use, the
Withdrawn Assets shall remain held in the Company Treasury Vault.

Informative note (non-binding): Subject to later governance approval, the
Withdrawn Assets may support broader exchange access, professional
market-making arrangements, new trading venues, ecosystem rewards, and other
initiatives connected to Solomon's launch and growth.

---

## 8. Binding execution constraints

**RESOLVED:** The Treasury Executor must implement this Resolution subject to
the following constraints:

1. **Complete withdrawal:** the DAO's entire liquidity position in the Pool
   must be withdrawn, subject only to de minimis residual dust.
2. **No leverage:** no borrowing, margin, leverage, or derivatives may be
   used.
3. **No trading:** no swap or trade is authorized as part of execution.
4. **No interim use:** the Withdrawn Assets may not be used between withdrawal
   and transfer to the Company Treasury Vault.
5. **Prohibited behavior:** no wash trading or transaction intended to mislead
   market participants is permitted.
6. **Scope limitation:** no other liquidity pool, vault, staking position, or
   DAO-controlled asset may be withdrawn from or otherwise affected.

---

## 9. Residual dust and execution record

### 9.1 Residual dust

**RESOLVED:** If a de minimis residual balance remains because of rounding,
minimum withdrawal thresholds, or another technical limitation that makes
withdrawal economically impractical, the residual will not constitute a
failure to execute this Resolution.

### 9.2 Execution record

**RESOLVED:** The governance record shall disclose:

- the execution transaction signature or signatures;
- the actual amount of SOLO withdrawn and transferred;
- the actual amount of USDC withdrawn and transferred, if any; and
- any residual dust left in the Pool or the DAO's liquidity position.

---

**Disclaimer (Governance Proposal; No Professional Advice).**

This document is a governance proposal and governance communication.
If adopted by the DAO through its governance mechanisms, it may become
binding on the DAO and persons exercising authority under the
Company Agreement to the extent provided in the Company Agreement and
applicable law.
This document does not constitute legal, tax, financial, or other
professional advice.
The author(s) are not acting as legal counsel to the DAO or any
member or user. No attorney-client relationship is created.

You must obtain your own independent advice for your circumstances.
