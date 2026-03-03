# SOP: Order of Business for Operational Packs

**Status:** Pre-formation (executed by Organizer; not adopted by on-chain vote)

**Effectiveness:** This SOP takes effect on the Effective Date of the Company's Certificate of Formation.

**TERTIARY INSTRUMENT.** This SOP is a tertiary instrument of the Company Agreement and is maintained in the SOP Registry.

**Not a Registrar Registry.** This SOP and the SOP Registry are internal governance instruments of the Company. They are not the registry maintained by the Registrar of Corporations, the Marshall Islands DAO LLC Registry, or the IRI Registry. This SOP does not replace or purport to be any Registrar-maintained registry.

**Normative Identifier.** SOP-00000

---

## Intellectual Property Firewall

**"Protocol"** in this SOP, the SOP Registry, and SOP Registry entries has the same meaning as **"Protocol IP"** as defined in Operating Agreement §2.1(17) - design, documentation, code, repositories, and other intellectual property. It does not mean an operating business, service, issuer, custodian, counterparty, or other person or entity.

---

## 1. Purpose

This SOP defines how the Company adopts, amends, and periodically ratifies standard operating procedures without requiring a full governance cycle for every operational change.

---

## 2. Document Hierarchy

The Company Agreement comprises:

- **Primary Instruments:** the Operating Agreement, the Founding Charter, and the IP License Framework;
- **Secondary Instruments:** the Smart Contract Registry, Website Registry, Intellectual Property Registry, IP License & Assignment Register, and the Counterparty Agreements Register; and
- **Tertiary Instruments:** this SOP, and the SOP Registry.

In the event of conflict, the order of precedence established in the Operating Agreement applies.

Tertiary Instruments may not expand authority beyond what Primary and Secondary Instruments and on-chain constraints permit.

---

## 3. Interim Adoption

The Head Steward may adopt or amend SOPs on an interim basis within existing authority. Subcommittees may adopt or amend SOPs within their existing authority and defined scope (Founding Charter §8.2). Either may rely on drafts or inputs prepared by Subcommittees or delegates acting within their mandates.

Interim SOPs:

1. bind only within the scope of existing authority;
2. do not create obligations for Members beyond existing obligations;
3. do not grant new rights to access or move Company Treasury Accounts; and
4. do not modify Primary or Secondary Instruments.

---

## 4. Periodic Ratification

The Company should ratify SOP changes through periodic Operational Pack proposals. Each Operational Pack should include:

1. **Scope statement.** Categories of SOPs covered.
2. **Change log.** Summary of additions, removals, and material changes.
3. **Content identifiers.** Hashes or content identifiers for each SOP.
4. **Effective date.** When the ratified pack becomes effective.
5. **Review date.** When the next pack is expected.

---

## 5. Standard Order of Business

Unless a proposal specifies otherwise:

1. Notice and agenda.
2. Eligibility checks.
3. Disclosures (conflicts and material implications, subject to confidentiality).
4. Resolution text.
5. Execution Bundle review.
6. Risk checks.
7. Voting and adoption.
8. Execution and post-execution reporting.

---

## 6. Confidentiality

This SOP does not require public disclosure of Confidential Information or Security-Sensitive Information. The Company may rely on:

1. on-chain constraints;
2. independent audits and attestations; and
3. post-facto reporting.

---

## 7. Confidential Entries

The SOP Registry may include confidential entries recorded by:

1. a confidential hash or content identifier; and
2. metadata sufficient for integrity verification.

Confidential entries do not grant membership, voting rights, economic rights, or authority beyond existing on-chain constraints.

Full particulars are disclosed only:

1. to a confidential reviewer or auditor under appropriate controls; or
2. in response to a lawful legal request.

---

## 8. Recordkeeping

Each ratified Operational Pack should be recorded with its content identifiers and effective date.

The SOP Registry maintains the current ratified versions of governance instruments. Superseded versions are retained for auditability.

---

## 9. Canonical Locations

**Proposal Repository.** The proposal repository is the canonical source for proposal history, drafts, and execution artefacts:
- https://github.com/SolomonDAOrg/dao-proposals

**SOP Registry.** The SOP Registry is the canonical source for current ratified versions of governance instruments:
- https://github.com/SolomonDAOrg/sop-registry

**Record Schema and Tooling.** The Company adopts a Record Schema used to describe and validate governance records and registry entries. The canonical references are:
- https://github.com/SolomonDAOrg/record-schema
- https://github.com/SolomonDAOrg/record-schema-toolkit

Each repository's LICENSE governs its contents. The Record Schema and Toolkit are Protocol IP. Public availability does not constitute a license to use, reproduce, or adapt without authorization.

The Company may change, migrate, or replace these locations by Resolution.

---

## 10. Confidential Placeholder Records

The SOP Registry may include a Confidential Placeholder Public Key (CPPK) record that publishes:

1. the public key (ed25519; not a program ID or PDA);
2. the role;
3. the scope (spending limits, caps, destination allowlists); and
4. a confidential hash binding the counterparty particulars.

A CPPK record does not grant membership, voting rights, economic rights, or authority. Any authority exists only through on-chain spending limits and program constraints.

The counterparty must be able to prove control of the private key by producing a signature over a standardized challenge message. The attestation may be published or lodged as a confidential instrument.

Counterparty particulars are disclosed only:

1. to a confidential reviewer or auditor under appropriate controls; or
2. in response to a lawful legal request.

---

## 11. Amendment

This SOP is a Tertiary Instrument. It may be amended on an interim basis by the Head Steward or by Subcommittees acting within their existing authority (Founding Charter §8.2), in accordance with §6.5(4) of the Operating Agreement. Such amendments must be recorded in the SOP Registry and are subject to objection by Resolution.

No amendment is effective until any required Execution Bundle is executed and the amended instrument is recorded in the SOP Registry in accordance with the Founding Charter.