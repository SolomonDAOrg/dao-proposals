# DP-00002: SOLO Buyback Framework and Governance Threshold Update

**Status:** Draft (intended for ratification via Governance System)

**Version:** 1.0.0

**Owner:** SOLOMON DAO LLC (via Governance System)

**Applies to:** DAO governance participants; persons executing treasury transactions under existing DAO authority; custodians of Buyback Vault.

**Effective date:** Upon ratification by Governance System **and** successful on-chain execution of the Execution Bundle (as defined below).

**Confidentiality classification:** Public (operational/security-sensitive details may be handled under appropriate confidentiality controls)

**Supersedes:** None

**Related:** DP-00001 (pre-formation designates + legal budget); DP-00003 (post-formation activation + company account designation)

---

## Intellectual Property Firewall

**"Protocol"** in this Resolution has the same meaning as **"Protocol IP"** as defined in the Company Agreement of SOLOMON DAO LLC (Operating Agreement §2.1(17)) -- design, documentation, code, repositories, and other intellectual property. It does not mean an operating business, service, issuer, custodian, counterparty, or other person or entity.

Nothing in this Resolution authorizes the Company, the Head Steward, or any Subcommittee to direct, supervise, or control the operations of any Licensee, counterparty, service provider, or other person. Any external obligations arise only under the applicable License or other written agreement, and only to the extent expressly stated there.

---

## 1. Purpose

This Resolution does two things:

1. Updates governance thresholds/parameters (on-chain).  
2. Authorizes and funds a capped SOLO buyback program (on-chain), with binding constraints and reporting.

---

## 2. Operative rule

This is normative text proposed for adoption by Governance System. If (and only if) it is adopted and the Execution Bundle executes successfully, the operative clauses below are effective as stated.

---

## 3. Definitions

1. **"Buyback Program"** means the capped SOLO buyback program authorized by this Resolution.

2. **"Buyback Vault"** means the wallet/vault specified in §6.2 that will receive stable funds for buyback operations.

3. **"Execution Bundle"** means the on-chain transactions that implement the on-chain portions of this Resolution.

4. **"Governance System"** means the on-chain mechanism by which this Resolution is adopted and executed.

5. **"SOLO"** means the SOLO token (mint/address: `SoLo9oxzLDpcq1dpqAgMwgce5WqkRDtNXK7EPnbmeta`).

6. **"Stable Asset"** means `USDC` (mint/address: `EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v`).

7. **"Treasury Executor"** means the existing DAO treasury execution authority that can lawfully execute on-chain treasury operations today (e.g., current treasury multisig / authorized operators under current governance).

---

## 4. Governance threshold update (on-chain)

**RESOLVED:** Governance System parameters are updated as follows (the "Threshold Update"):

- quorum: `[TBD]`
- approval_threshold: `[TBD]`
- voting_period: `[TBD]`
- execution_delay_or_timelock: `[TBD]`
- proposal_creation_threshold: `[TBD]`
- any additional parameters: `[TBD]`

**RESOLVED:** The Threshold Update is effective immediately upon successful execution of the Execution Bundle.

---

## 5. SOLO buyback authorization (policy + cap)

### 5.1 Authorization

**RESOLVED:** The DAO authorizes the Buyback Program, subject to the binding constraints in §7.

### 5.2 Cap and window

**RESOLVED:** The Buyback Program is capped as follows:
- max spend (Stable Asset): **`[TBD MAX_SPEND]`**
- program window: `[TBD start date/time]` to `[TBD end date/time]`

### 5.3 Custody of acquired SOLO

**RESOLVED:** SOLO acquired under the Buyback Program shall be held in:
- **SOLO Treasury Wallet / Vault:** `[TBD]`
(or specify that the Buyback Vault will custody SOLO directly: `[TBD]`)

---

## 6. Buyback Vault funding (on-chain)

### 6.1 Buyback Vault designation

**RESOLVED:** The Buyback Vault is designated as:
- **Buyback Vault / Vault ID:** `[TBD address / vault id]`

### 6.2 Transfer instruction (Execution Bundle)

**RESOLVED:** The Execution Bundle shall transfer up to **`[TBD MAX_SPEND]`** of Stable Asset from DAO treasury to the Buyback Vault.

---

## 7. Binding execution constraints (must comply)

**RESOLVED:** The Treasury Executor must execute the Buyback Program in compliance with all constraints below:

1. **No leverage:** no borrowing, margin, leverage, or derivatives to implement buybacks.  
2. **Dispersed execution:** purchases must be dispersed over time (TWAP/DCA).  
3. **Max order size:** no single purchase may exceed **`[TBD MAX_ORDER_NOTIONAL]`** Stable Asset.  
4. **Permitted venues/routes:** only the following venues/routes are permitted: `[TBD allowlist]`.  
5. **Prohibited behavior:** no wash trading; no trades intended to mislead market participants.  
6. **Price discipline (optional):** only execute within stated bands/conditions: `[TBD, or "none"]`.  
7. **Cap enforcement:** cumulative Stable Asset spent must not exceed **`[TBD MAX_SPEND]`**.

---

## 8. Reporting (binding)

**RESOLVED:** A public report shall be posted at least every `[TBD cadence, e.g. 7 days]` during the program window and once at completion, including:
- total Stable Asset spent (cumulative)
- total SOLO acquired (cumulative)
- average purchase price (time-weighted where reasonable)
- ending balances of Buyback Vault and SOLO Treasury Wallet
- transaction identifiers / links

---

## 9. Execution Bundle scope limitation (binding)

**RESOLVED:** The Execution Bundle for DP-00002 shall include only:
- the Threshold Update in §4, and
- the Buyback Vault funding transfer in §6.2.

**RESOLVED:** The Execution Bundle for DP-00002 shall not include:
- any Company-account designation,
- any post-formation Treasury Subcommittee authority activation,
- any transfers of main treasury into a Company Treasury Account (that is DP-00003),
- any legal budget release (that is DP-00001).

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