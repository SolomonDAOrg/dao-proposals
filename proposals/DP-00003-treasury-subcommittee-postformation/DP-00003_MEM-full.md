# DP-00003: Post-Formation Treasury Subcommittee Activation; Company Treasury Account Designation; Initial Treasury Transfer

**Status:** Draft (intended for ratification via Governance System)

**Version:** 1.0.0

**Owner:** SOLOMON DAO LLC (via Governance System)

**Applies to:** DAO governance participants; Treasury Subcommittee members; signers/operators of the Company Treasury Vault; persons handling Confidential Information under Undertakings.

**Effective date:** Upon (i) Company formation being effective, and (ii) ratification by Governance System **and** successful on-chain execution of the Execution Bundle (as defined below).

**Confidentiality classification:** Public (operational/security-sensitive details may be handled under Undertakings and kept confidential)

**Supersedes:** None

**Related:** DP-00001 (designates + legal budget); DP-00002 (buyback + governance thresholds); CON-00001 (Treasury Subcommittee Undertaking/NDA)

---

## Intellectual Property Firewall

**"Protocol"** in this Resolution has the same meaning as **"Protocol IP"** as defined in the Company Agreement of SOLOMON DAO LLC (Operating Agreement §2.1(17)) -- design, documentation, code, repositories, and other intellectual property. It does not mean an operating business, service, issuer, custodian, counterparty, or other person or entity.

Nothing in this Resolution authorizes the Company, the Head Steward, or any Subcommittee to direct, supervise, or control the operations of any Licensee, counterparty, service provider, or other person. Any external obligations arise only under the applicable License or other written agreement, and only to the extent expressly stated there.

---

## 1. Purpose

This Resolution is the **post-formation activation** step. It:

1. Confirms a second multisig/vault as an official **Company Treasury Account**.  
2. Grants the Treasury Subcommittee delegated authority over designated Company Treasury Accounts only.  
3. Transfers an initial tranche of assets from the main DAO treasury into the Company Treasury Account.  
4. Imposes minimum mechanical constraints and reporting requirements.

---

## 2. Operative rule

This is normative text proposed for adoption by Governance System. If (and only if) it is adopted and the Execution Bundle executes successfully, the operative clauses below are effective as stated, **subject to the Formation Condition**.

---

## 3. Definitions

1. **"Company"** means SOLOMON DAO LLC.

2. **"Company Treasury Account"** means a treasury account/vault designated by Governance System as a Company account for Company treasury operations.

3. **"Company Treasury Vault"** means the multisig/vault specified in §6.1.

4. **"Execution Bundle"** means the on-chain transactions that implement the on-chain portions of this Resolution.

5. **"Formation Condition"** means the Company’s formation is legally effective on or before execution of the Execution Bundle.

6. **"Governance System"** means the on-chain mechanism by which this Resolution is adopted and executed.

7. **"Treasury Subcommittee"** means the Company treasury subcommittee contemplated by the Company Agreement framework.

8. **"Treasury Subcommittee Members"** means the members appointed/designated by governance (DP-00001) and finalized herein if needed.

9. **"Treasury Operating Policy"** means the binding constraints in §7 (and any referenced policy annex by hash/link).

10. **"Undertaking"** means the Treasury Subcommittee confidentiality undertaking.

---

## 4. Formation condition (hard gate)

**RESOLVED:** No designation of a Company Treasury Account, no grant of delegated authority, and no initial treasury transfer under this Resolution is effective unless the Formation Condition is satisfied.

**RESOLVED:** Formation evidence must be published as:
- certificate / registry evidence link, and/or
- content hash/anchor of the formation evidence.
`[TBD: link or hash]`

---

## 5. Treasury Subcommittee activation (delegated authority; limited scope)

### 5.1 Grant of delegated authority (Company accounts only)

**RESOLVED:** Subject to the Formation Condition, the Treasury Subcommittee is granted delegated authority to manage **only** the Company Treasury Account(s) designated by Governance System, strictly within the Treasury Operating Policy constraints.

**RESOLVED:** The Treasury Subcommittee has **no authority** over any DAO treasury accounts that are not expressly designated as Company Treasury Accounts.

### 5.2 Membership and undertakings

**RESOLVED:** Treasury Subcommittee Members are:
- Member A: `[name/handle]` -- `[wallet]`
- Member B: `[name/handle]` -- `[wallet]`
- Member C: `[name/handle]` -- `[wallet]`

**RESOLVED:** Each Member must have an executed Undertaking as a condition precedent to receiving Confidential Information.

---

## 6. Company Treasury Account designation (second multisig/vault)

### 6.1 Designation

**RESOLVED:** Subject to the Formation Condition, the following vault is designated as a **Company Treasury Account** (the "Company Treasury Vault"):
- **Company Treasury Vault / Vault ID:** `[TBD address / vault id]`

### 6.2 Signers and threshold (mechanical constraint)

**RESOLVED:** The signer set and threshold for the Company Treasury Vault shall be:
- signers: `[TBD wallets]`
- threshold: `[TBD]`
- optional roles/separation: `[TBD: proposer/executor separation if supported]`

---

## 7. Treasury Operating Policy (binding minimum constraints)

**RESOLVED:** The Treasury Subcommittee’s delegated authority is constrained by the following minimum controls:

1. **Account scope:** only designated Company Treasury Account(s).  
2. **Per-txn cap:** `≤ [TBD]` notional (or asset-specific caps).  
3. **Per-period cap:** `≤ [TBD]` per `[day/week]`.  
4. **Allowlists:** permitted programs/venues/routes/contracts: `[TBD allowlist]`.  
5. **Revocation:** Governance System may revoke/modify permissions, rotate signers, and/or freeze operations via subsequent proposal or emergency process `[TBD if any]`.  
6. **No leverage:** no borrowing/margin/leverage unless explicitly authorized by governance.  
7. **Recordkeeping:** every outbound movement must have a recorded rationale and tx reference; exceptions must be flagged.

---

## 8. Initial treasury transfer into Company Treasury Vault (on-chain)

**RESOLVED:** Subject to the Formation Condition, the Execution Bundle shall transfer the following assets from the main DAO treasury into the Company Treasury Vault:

- asset_1 (mint): `[TBD]` -- amount: `[TBD]`
- asset_2 (mint): `[TBD]` -- amount: `[TBD]`
- optional total notional cap: `[TBD]`

---

## 9. Reporting (binding)

**RESOLVED:** The Treasury Subcommittee shall publish a public report every `[TBD cadence]` including:
- balances (start/end) of the Company Treasury Vault
- inflows/outflows by asset
- executed transactions / identifiers
- confirmations of policy compliance (caps/allowlists)
- any incidents / exceptions and remediation

---

## 10. Execution Bundle scope limitation (binding)

**RESOLVED:** The Execution Bundle for DP-00003 shall include only:
- designation/configuration references for the Company Treasury Vault (as supported on-chain), and
- any on-chain delegation/authority steps required (if applicable), and
- the initial treasury transfer(s) in §8.

**RESOLVED:** The Execution Bundle for DP-00003 shall not include:
- governance threshold updates (that is DP-00002),
- buyback operations (that is DP-00002),
- legal budget release (that is DP-00001).

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