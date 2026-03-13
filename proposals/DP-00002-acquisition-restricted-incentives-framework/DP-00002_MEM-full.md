# DP-00002: SOLO Acquisition and Restricted Incentives Reserve Framework

**Status:** Draft (intended for ratification via Governance System)

**Version:** 1.0.2

**Owner:** SOLOMON DAO LLC (via Governance System)

**Applies to:** DAO governance participants; persons executing treasury
transactions under existing DAO authority; custodians of the Acquisition
Facility and any DAO treasury wallet or vault holding acquired SOLO;
any later approved Incentives Subcommittee or substantially similar
successor body.

**Effective date:** Upon ratification by Governance System **and** successful
on-chain execution of the Execution Bundle (as defined below).

**Authority note:** This Resolution authorizes acquisition and reserve
designation only. It does not establish the live Incentives Subcommittee,
appoint its members, or grant present authority to distribute, commit,
allocate, sell, transfer, make claimable, or otherwise deploy Restricted
SOLO Incentives Reserve assets.

**Confidentiality classification:** Public (operational/security-sensitive
details may be handled under appropriate confidentiality controls)

**Supersedes:** None

**Related:** DP-00001 (pre-formation treasury designates + legal budget);
any later proposal establishing the live Incentives Subcommittee; any later
proposal activating pips or any substantially similar successor participation
based framework.

---

## Intellectual Property Firewall

**"Protocol"** in this Resolution has the same meaning as **"Protocol IP"**
as defined in the Company Agreement of SOLOMON DAO LLC (Operating Agreement
§2.1(17)) -- design, documentation, code, repositories, and other
intellectual property. It does not mean an operating business, service,
issuer, custodian, counterparty, or other person or entity.

Nothing in this Resolution authorizes the Company, the Head Steward, or
any Subcommittee to direct, supervise, or control the operations of any
Licensee, counterparty, service provider, or other person. Any external
obligations arise only under the applicable License or other written
agreement, and only to the extent expressly stated there.

---

## 1. Purpose

This Resolution does two things:

1. Authorizes and funds a capped SOLO acquisition program (on-chain), with
   binding constraints and required reporting.
2. Requires that all SOLO acquired under that program be retained and
   separately accounted for as **Restricted SOLO Incentives Reserve**
   property pending later governance activation.

---

## 2. Operative rule

This is normative text proposed for adoption by Governance System. If (and
only if) it is adopted and the Execution Bundle executes successfully,
the operative clauses below are effective as stated.

---

## 3. Definitions

1. **"Acquisition Facility"** means the recurring order, vault, wallet,
   or other execution arrangement specified in §5.1 that is used to
   implement the authorized SOLO acquisition program.

2. **"Acquisition Program"** means the capped SOLO acquisition program
   authorized by this Resolution.

3. **"Execution Bundle"** means the on-chain transactions that implement
   the on-chain portions of this Resolution.

4. **"Governance System"** means the on-chain mechanism by which this
   Resolution is adopted and executed.

5. **"Incentives Subcommittee"** means the contemplated post-formation
   company-side incentives subcommittee, if later established or activated
   by governance.

6. **"Restricted SOLO Incentives Reserve"** means the SOLO acquired under
   this Resolution and designated for the Designated Purpose described
   in §4.4.

7. **"SOLO"** means the SOLO token (mint/address:
   `SoLo9oxzLDpcq1dpqAgMwgce5WqkRDtNXK7EPnbmeta`).

8. **"Stable Asset"** means `USDC` (mint/address:
   `EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v`).

9. **"Treasury Executor"** means the existing DAO treasury execution
   authority that can lawfully execute on-chain treasury operations today
   (e.g. current treasury multisig / authorized operators under current
   governance).

10. **"TWAP"** means time-weighted average price.

---

## 4. SOLO acquisition authorization and reserve designation

### 4.1 Authorization

**RESOLVED:** The DAO authorizes the Acquisition Program, subject to the
binding constraints in §6.

### 4.2 Cap and window

**RESOLVED:** The Acquisition Program is capped as follows:
- max spend (Stable Asset): **`1,000,000 USDC`**
- program duration: **up to 60 days** from commencement

### 4.3 Maximum program TWAP and estimated acquisition

**RESOLVED:** The effective aggregate program TWAP for SOLO acquired under
the Acquisition Program must not exceed **`0.74 USDC per SOLO`**.

**RESOLVED:** On the assumption that the full spend cap is used at the
maximum permitted program TWAP, the Acquisition Program would acquire
approximately **`1,351,351.35 SOLO`**, before fees, slippage, routing
differences, and any unspent residual Stable Asset.

### 4.4 Custody, reserve status, and designated purpose

**RESOLVED:** All SOLO acquired under the Acquisition Program shall be
retained in DAO treasury custody and designated on the DAO's books and
records as **Restricted SOLO Incentives Reserve** property.

**RESOLVED:** The Designated Purpose of the Restricted SOLO Incentives
Reserve is to support SOLO-backed incentive programs intended to reward
participation, deepen alignment, and support long-term ecosystem growth,
including pips and any substantially similar successor or related
participation based framework later approved by governance.

**RESOLVED:** pips, and any substantially similar successor participation
framework approved by governance, shall have first call priority on the
Restricted SOLO Incentives Reserve.

**RESOLVED:** Until amended by express later governance action, the
Restricted SOLO Incentives Reserve shall remain earmarked for its
Designated Purpose and shall not be repurposed, redirected, impaired, or
clawed back by any signer, contributor, service provider, committee,
operator, or other person acting without such governance approval.

---

## 5. Acquisition Facility funding and implementation

### 5.1 Acquisition Facility designation

**RESOLVED:** The Acquisition Facility may consist of a Jupiter recurring
order or other substantially similar recurring on-chain execution
arrangement consistent with this Resolution.

**RESOLVED:** The specific Acquisition Facility wallet, order account,
vault, or related execution address may be designated in the Execution
Bundle or related implementation instructions, provided the facility
remains subject to this Resolution.

### 5.2 Transfer instruction (Execution Bundle)

**RESOLVED:** The Execution Bundle shall transfer up to **`1,000,000 USDC`**
of Stable Asset from DAO treasury to the Acquisition Facility.

### 5.3 Treatment of unspent Stable Asset

**RESOLVED:** Any Stable Asset not spent under the Acquisition Program
remains DAO treasury property and shall be returned to, or continuously
recognized as held for, DAO treasury.

---

## 6. Binding execution constraints (must comply)

**RESOLVED:** The Treasury Executor must execute the Acquisition Program in
compliance with all constraints below:

1. **No leverage:** no borrowing, margin, leverage, or derivatives may be
   used to implement acquisitions.

2. **Dispersed execution:** acquisitions must be dispersed over time using
   recurring or otherwise time-distributed execution rather than a single
   discretionary block purchase.

3. **Operational sizing and cadence:** order sizing, frequency, and interval
   may vary during the approved window, provided execution remains
   recurring/dispersed and all other constraints in this Resolution are met.

4. **Price discipline:** the effective aggregate program TWAP must not
   exceed **`0.74 USDC per SOLO`**.

5. **Prohibited behavior:** no wash trading; no trades intended to mislead
   market participants.

6. **Cap enforcement:** cumulative Stable Asset spent must not exceed
   **`1,000,000 USDC`**.

7. **Window enforcement:** execution must cease no later than the end of the
   approved 60 (sixty) day program duration unless completed earlier because
   the cap is exhausted.

8. **Transfer of acquired SOLO:** acquired SOLO must be transferred promptly
   to DAO treasury custody, unless the Acquisition Facility itself is
   expressly designated as that custody location.

9. **No unauthorized deployment:** no acquired SOLO may be distributed,
   sold, lent, pledged, staked, paired for liquidity, used as collateral,
   used as market making inventory, used for compensation, or otherwise
   deployed except as expressly permitted by this Resolution or by later
   governance action.

---

## 7. Reporting (binding)

**RESOLVED:** A public report shall be posted at reasonable intervals during
the program window and once at completion, including:

- total Stable Asset spent (cumulative)
- total SOLO acquired (cumulative)
- total SOLO retained as Restricted SOLO Incentives Reserve (current balance)
- effective average acquisition price, including time-weighted treatment
  where reasonably available
- ending balances of the Acquisition Facility and relevant treasury custody
  location(s)
- transaction identifiers / links

---

## 8. No current deployment authority

**RESOLVED:** This Resolution does not establish the live Incentives
Subcommittee or appoint its members.

**RESOLVED:** This Resolution does not authorize any person or body to
distribute, commit, allocate, sell, transfer, make claimable, or otherwise
deploy Restricted SOLO Incentives Reserve assets at this time.

**RESOLVED:** Until later governance action establishes and approves the
live Incentives Subcommittee and any applicable activation framework,
reserve SOLO shall remain held in DAO treasury custody and accounted for
solely for its Designated Purpose.

---

## 9. Core guardrails

Unless expressly approved by later governance action:

- reserve SOLO shall remain held in DAO treasury custody and separately
  accounted for as Restricted SOLO Incentives Reserve property;
- reserve SOLO may not be self-dealt, privately allocated, or directed to
  insiders or affiliates on preferential terms;
- reserve SOLO may not be manually transferred wallet to wallet to selected
  recipients as a discretionary allocation method;
- reserve SOLO may not be sold or otherwise disposed of below prevailing
  market price;
- reserve SOLO may not be lent, pledged, staked, paired for liquidity,
  used as collateral, used as market making inventory, or used for
  compensation; and
- any unused, expired, forfeited, cancelled, or unclaimed reserve SOLO shall
  be burned unless governance expressly directs otherwise.

---

## 10. Future governance

A later governance action may establish the live Incentives Subcommittee,
appoint or approve its members, adopt activation controls, approve claims
mechanics or other distribution logic, and authorize deployment of
Restricted SOLO Incentives Reserve assets for the Designated Purpose.

Until that later governance action is adopted, no signer, contributor,
service provider, committee, operator, or other person may rely on this
Resolution as authority to deploy reserve SOLO.

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
