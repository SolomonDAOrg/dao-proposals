# SOLOMON DAO LLC - DAO Proposal Documentation Convention

This repository holds long-form documentation and execution
artefacts for DAO proposals.

The goals:

-   Preserve a clean, chronological history of proposals.
-   Make it obvious which files are the canonical memorandum, charter,
    supporting records, and execution bundles.
-   Track status (draft, voting, executed, superseded) in a machine-readable
    way.

The conventions below are recommended but not mandatory. Proposals that do
not follow this scheme are still valid if they pass governance; they may,
however, be harder to index and audit.

## Canonical pinning on adoption (MANDATORY)

When a proposal is **adopted** (i.e. it reaches `status.phase` = `passed` or
later), it MUST be pinned to an **annotated git tag** that captures the
governance outcome and the exact text that was adopted.

**Required steps on adoption:**

1. **Create an annotated tag** pointing at the adopted commit. The tag
message MUST include:

    - governance vote reference (e.g. MetaDAO proposal number);
    - voting outcome (passed/rejected/withdrawn/expired);
    - any on-chain execution references (tx signature(s), bundle hash,
      etc.);
    - the full commit hash (or the tag is itself sufficient if it points
      to the commit).

2. **Record the pin in `META.yaml`** (same proposal directory):

    - `extensions.dao_proposals.governance.passed_commit` = full git commit hash;
    - `extensions.dao_proposals.governance.passed_tag` = the annotated tag name;
    - `extensions.dao_proposals.governance.passed_pinned` = UTC timestamp;
    - `extensions.dao_proposals.governance.vote.reference` /
      `extensions.dao_proposals.governance.vote.tx_refs` /
      `extensions.dao_proposals.governance.discussion_urls` as applicable;
    - `extensions.dao_proposals.governance.execution_txs` (list) where applicable.

3. **Record the same in `LOG-governance.md`** (append-only event log).

4. **Do not edit adopted text in-place.** Corrections/amendments require a
   **new proposal ID** that `supersedes` the prior proposal.

**Tag naming (recommended):**

-   `DP-00001@adopted-YYYY-MM-DD` (simple and readable), or
-   `DP-00001@passed-MetaDAO-123` (vote-centric)

Use **annotated** tags (not lightweight tags) so the tag itself carries
the vote/tx metadata.

---

## Disclaimer

This repository is a publication and coordination venue for governance
artefacts. Repository Materials are **not** legal, tax, investment, or other
professional advice, and proposals may be authored by anyone (subject to the
contribution terms in LICENSE and CONTRIBUTING.md).

Some proposals, if adopted through the DAO's governance mechanisms,
may become **binding on the DAO and persons exercising authority under
the Company Agreement** (and may be executed on-chain and/or filed with
service providers).
That governance effect does not make the repository "legal advice" for
anyone else.

The canonical record of what was adopted is the DAO's governance system /
on-chain record, the SOP Registry, and any executed or filed instruments (as
applicable). If a repository copy differs, the adopted record controls.

See: `DISCLAIMER.md` and `LICENSE`.

---

## Confidential filings, forms, and identity materials (NOT repository content)

Some filings require government forms, KYC/identity documents, wet-signed originals, or third-party service-provider paperwork.

- Do **not** commit government originals or identity artefacts into this repository.
- Instead, record only **evidence anchors** (hash/CID + short label) in `META.yaml` under `commitments` or equivalent metadata.
- Treat these artefacts as third-party/government/individual property, not as DAO governance records.

This keeps the proposal registry clean, auditable, and safe to publish.

---

## License

Copyright (C) 2026 **SOLOMON DAO LLC**, a Marshall Islands DAO LLC organized
under the Decentralized Autonomous Organizations Act of 2022 as amended.

Repository Materials are Protocol IP (as defined in the Company Agreement).
See `LICENSE` (SOLOMON DAO LLC PUBLIC GOVERNANCE REPOSITORY LICENSE v1.0).
See `DISCLAIMER.md` (no advice; no endorsement; required `MEM` footer).
MetaDAO Cohorts have a reuse license for governance and templates under
LICENSE Section 4. No trademark or Protocol production-use rights are
granted here.

---

## 1. Directory layout

Each proposal lives in its own directory:

```text
dao-proposals/
  INDEX.md
  DP-00001-example-slug-charter/
  DP-00002-incentive-program/
  ...
```

-   `DP` = "DAO Proposal".
-   `00001` = zero-padded integer series ID (strict ordering).
-   The trailing slug (`example-name-here`) is a short, kebab-cased human
    label.

Example proposal directory:

```text
DP-00001-example-name-here/
  DP-00001_META.yaml
  DP-00001_IND-index.md
  DP-00001_MEM-summary.md
  DP-00001_MEM-full.md
  DP-00001_CHA-example-founding-charter.md
  DP-00001_TX-main.json
  DP-00001_TX-main.borsh
  DP-00001_LOG-governance.md
```

---

## 2. Proposal ID

**Format:** `DP-XXXXX`

-   `DP-00001`, `DP-00002`, ...
-   IDs are never reused.
-   If a proposal is replaced or corrected, it gets a new ID and uses the
    `supersedes` / `superseded_by` linkage in `META.yaml` (see below).

**DP-00000 (reserved genesis / formation packet):**

-   `DP-00000` is reserved for the pre-formation organizer record (founding
    instrument pack / filing packet).
-   It is **not** a governance vote artefact (no on-chain vote is possible
    pre-formation).
-   Use `status.phase: preformation` while filing is in progress (entity
    not yet formed), then advance to `status.phase: formation` once the
    entity is formed and the filing is complete.
-   Track filing/formation outcomes as submission evidence, not as votes.

---

## 3. File types and naming

Each file starts with the proposal ID and a three-letter document type code:

```text
<PROPOSAL_ID>_<DOC_TYPE>-<short-description>.<ext>
```

### 3.1 Document type codes

-   `MEM` - **Memorandum**
    The English narrative that describes the proposal and maps to any
    execution or filing steps.
    MUST include the standard disclaimer footer (see DISCLAIMER.md).

-   `CHA` - **Charter / Primary Instrument**
    A durable charter or other primary company instrument adopted, amended,
    or carried by the record.

-   `ANN` - **Annex / Appendix**
    Technical specifications, parameters, state-machine descriptions,
    schedules, proofs, etc.

-   `SOP` - **Standard Operating Procedure**
    Operational governance procedures (rare in normal proposals; used in
    formation packs).

-   `SUPP` - **Supplement**
    Supplemental, non-primary narrative or supporting material.

-   `REG` - **Register / Registry**
    A tabular/list document (a “register”) maintained as a canonical
    registry artefact.
    Examples: Smart Contract Register, Website Register. Where this
    repository references the DAO Act phrase "directly manages,
    facilitates, or operates", that is a statutory classification - not an
    admission of day-to-day operation.

-   `TX` - **Execution Bundle**
    Encoded on-chain transactions that implement the proposal (e.g.,
    Squads payloads).
    These are usually evidence/implementation artefacts, not the filed
    instrument text.

-   `IND` - **Index (Table of Contents)**
    Human-readable index/TOC for a multipart record directory. Recommended
    for any record with multiple instruments/parts.

-   `PKT` - **Packet (Compiled Filing Artefact)**
    A derived, compiled submission artefact (typically a PDF) generated
    by stitching ordered Markdown parts.
    Not a canonical source document unless explicitly pinned/hashed
    in `META`.

-   `META` - **Metadata**
    Machine-readable status, IDs, timestamps, cross-links, and pack
    ordering (index/packet/precedence).

-   `LOG` - **Governance Log**
    Human-readable log of notes, commentary, and outcomes. Typically
    not part of a filed packet.

-   `DOC` - **Primary Document**
    Default primary document when no specialised narrative type applies.

-   `REP` - **Report**
    Audit report, incident report, review report.

-   `EVD` - **Evidence**
    Raw artefacts, exports, emails, screenshots, captures.

-   `IOC` - **Indicators**
    Indicators of compromise, blocklists, rules, hashes, addresses.

-   `POL` - **Policy**
    Policy record content.

-   `DAT` - **Data**
    Structured data attached to a record.

-   `DIA` - **Diagram**
    Chart or diagram source definition using record-schema-chart format.

> The canonical list of document type codes is maintained in
> `doc-types.yaml` (record-schema-registry format). The list above is a
> summary; consult the registry for recommended extensions, envelope IDs,
> and other metadata.

### 3.2 Examples

-   Main memorandum
    `DP-00001_MEM-full.md`

-   Summary memorandum
    `DP-00001_MEM-summarry.md`


-   On-chain execution bundle
    `DP-00001_TX-main.json`
    `DP-00001_TX-main.borsh`

-   Metadata
    `DP-00001_META.yaml`

-   Record index (per-record TOC)
    `DP-00001_IND-index.md`

-   Compiled filing packet (derived)
    `DP-00001_PKT-filing.pdf`

-   Governance log
    `DP-00001_LOG-governance.md`


### 3.3 Smart Contract Register / Registry (`REG`) documents

A `REG` document is the canonical smart contract register/registry
required under §106(2) of the RMI Decentralized Autonomous Organizations
Act 2022 (as amended).
It lists every smart contract on Solana that falls within the DAO Act
§106(2) classification for the Company, together with its program address, network,
governance / upgrade mechanics, and cross-references to the proposal set.

Each proposal that onboards, upgrades, or decommissions core contracts
SHOULD:

-   Include a `REG` file named:

```text
    <PROPOSAL_ID>_REG-smart-contract-registry.md
```

e.g. `DP-00001_REG-smart-contract-registry.md`.

-   State in a short preamble that the file "constitutes the Company's
    smart contract registry for purposes of §106(2) of the DAO Act" and
    that updates only take effect once approved by Resolution and, where
    required, implemented via the relevant `TX` bundle.

-   Contain a single primary Markdown table with one row per governed
    smart contract.

#### 3.3.1 Canonical table layout

The registry table MUST use the following columns in this order:

```markdown
| Registry ID | Contract Name / Module          | Program Address (base58)             | Network / Cluster   | Direct DAO Role (per §106(2))                | Governance / Upgrade Path                                      | Linked Record / DP Ref      | Notes / Detail      |
| ----------- | ------------------------------- | ------------------------------------ | ------------------- | -------------------------------------------- | -------------------------------------------------------------- | -------------------------- | ----------------------------------- |
| REG-001     | Governance Multisig (Squads v4) | XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX | Solana mainnet-beta | Directly manages DAO resolutions & execution | Upgradable via Governance System - Squads Exec Bundle DP-00001 | DP-00001; Charter §3E.6 | Primary on-chain governance control |
```

You then add one row per program:

-   **Registry ID**
    Stable row identifier (`REG-001`, `REG-002`, ...). When a contract is
    superseded, keep the old ID in the registry and update the Notes /
    Linked Record fields to show it is deprecated and what replaces it.

-   **Contract Name / Module**
    Human-readable name of the contract or module (e.g. "Governance
    Program", "Router", "Oracle").

-   **Program Address (base58)**
    Full Solana Program ID (base58). This MUST be the deployed Program ID
    actually governing assets or governance, not a dev build or draft.

-   **Network / Cluster**
    Exact Solana cluster (`mainnet-beta`, `devnet`, `localnet`, etc.).
    Main governance is normally on `mainnet-beta`; test / staging entries
    should be clearly labelled in Notes as non-governing.

- **Direct DAO Role (per §106(2))**
  Short description of how this program "directly manages, facilitates,
  within the §106(2) role classification for purposes of the DAO Act (e.g.
  "Program capability: treasury collateral custody; mint/burn logic",
  "Executes DAO resolutions and on-chain upgrades", "Routes liquidity
  incentives").
  Descriptions refer to program capabilities, not activities of
  the Company.

- **Governance / Upgrade Path**
  Who holds upgrade authority and how it is exercised (e.g.
  "Immutable", "Upgradable via Governance Multisig - Squads Exec
  Bundle", "Upgradeable only via timelocked DAO resolution").
  This should match the on-chain authority configuration and the
  `TX` bundles in the proposal.

- **Linked Record / DP Ref**
  Cross-references into the proposal set (e.g. "DP-00001; IP
  auditors jump from a program ID to its full technical spec.

- **Notes / Details**
  Any detail that is important but doesn't belong in the
  other columns: risk flags, planned deprecation, cluster-specific
  behaviour, or pointers to off-chain components that must stay in sync.

#### 3.3.2 Update rules

- The registry is updated only by passing a new DAO Proposal that
  ships a revised `REG` file and, where relevant, an updated `TX` bundle
  to enact the change on-chain.

- Proposals that migrate from one program ID to another SHOULD:
  - Add the new program as a new row; and
  - Mark the old one as deprecated in Notes, with a reference to the
    superseding proposal.

- The `META.yaml` file MAY also reference the `REG` file in its
  `documents` section so tooling can locate the canonical smart contract
  registry for a proposal.

---

## 4. Metadata and status (`META.yaml`)

Each proposal MUST have a single metadata file:

```text
DP-00001_META.yaml
```

This file is the **index and provenance anchor** for the proposal: it
links discussions, vote references, outcomes, and (critically) the
canonical git pins (**passed_tag** / **executed_tag**) that identify
the authoritative text.

For multipart records and filing packets, `META.yaml` also defines
canonical assembly via:

-   `documents.index` (per-record TOC)
-   `assembly.pack[]` (ordered stitch list with `precedence`)
-   `assembly.packet` (derived compiled packet path, e.g. PDF)

DAO-proposal-specific governance pins and vote/execution references
may live under `extensions.dao_proposals.*`.

### 4.1 Tightened schema (explicit pins + frozen adopted paths)

```yaml
schema: record-schema
schema_version: 1

id: DP-00001
series_code: DP
series: 1

title: Treasury Subcommittee (Pre-Formation) and Legal Budget
slug: treasury-subcommittee-preformation

authors:
  - name: "..."
    capacity: proposer

status:
  phase: draft # formation | preformation | draft | submitted | voting | passed | executed | failed | withdrawn | superseded
  last_updated: 2026-01-04T00:00:00Z

links:
  supersedes: []
  superseded_by: []
  related: []

documents:
  primary:
    - path: DP-00001_MEM-summary.md
      label: Summary memorandum
    - path: DP-00001_MEM-full.md
      label: Full memorandum
  secondary: []
  tertiary: []
  supplemental: []
  index:
    path: DP-00001_IND-index.md
  log:
    path: DP-00001_LOG-governance.md

assembly:
  packet:
    path: DP-00001_PKT-filing.pdf
    label: Compiled packet (derived)
  pack:
    - path: DP-00001_IND-index.md
      doc_type: IND
      precedence: 10
    - path: DP-00001_MEM-summary.md
      doc_type: MEM
      precedence: 20
    - path: DP-00001_MEM-full.md
      doc_type: MEM
      precedence: 30

timeline:
  opened_at: 2026-03-03T00:00:00Z
  drafted_at: 2026-03-03T00:00:00Z

extensions:
  formatting:
    profile: canonical-ascii
  language:
    locale: en-US

  dao_proposals:
    governance:
      proposal_number: 1
      proposer: null
      system: MetaDAO
      squads_dao_address: DzYtzoNvPbyFCzwZA6cSm9eDEEmxEB9f8AGkJXUXgnSA

      discussion_urls:                          # multiple threads allowed
        - "https://..."

      vote:
        reference: null                         # REQUIRED once phase >= voting (e.g. "MetaDAO#123")
        start: null                             # ISO-8601 UTC
        end: null                               # ISO-8601 UTC
        tx_refs: []                             # [{chain, network, signature, slot}]

      # Canonical pins -- passed stage
      passed_commit: null                       # REQUIRED once phase >= passed (full git hash)
      passed_tag: null                          # REQUIRED once phase >= passed (annotated tag)
      passed_pinned: null                       # REQUIRED once phase >= passed (ISO-8601 UTC)
      adopted_paths: []                         # REQUIRED once phase >= passed (freeze surface)

      # Canonical pins -- executed stage
      executed_commit: null                     # REQUIRED once phase == executed
      executed_tag: null                        # REQUIRED once phase == executed
      executed_pinned: null                     # REQUIRED once phase == executed
      execution_txs: []                         # [{chain, network, signature, slot}]

    result:
      outcome: pending_submission               # pending_submission | passed | failed | withdrawn | expired
      for_votes: null
      against_votes: null
      abstain_votes: null
      quorum_reached: null
      notes: null
```

**Populated example (phase = executed):**

```yaml
extensions:
  formatting:
    profile: canonical-ascii
  language:
    locale: en-US

  dao_proposals:
    governance:
      proposal_number: 1
      proposer: null
      system: MetaDAO
      squads_dao_address: DzYtzoNvPbyFCzwZA6cSm9eDEEmxEB9f8AGkJXUXgnSA

      discussion_urls:
        - "https://forum.solomondao.org/t/dp-00001"

      vote:
        reference: "MetaDAO#123"
        start: 2026-01-04T01:00:00Z
        end: 2026-01-06T01:00:00Z
        tx_refs:
          - chain: solana
            network: mainnet-beta
            signature: "..."
            slot: 123456789

      passed_commit: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"
      passed_tag: "DP-00001@passed-MetaDAO-123"
      passed_pinned: 2026-01-06T01:05:00Z
      adopted_paths:
        - DP-00001_MEM-full.md
        - DP-00001_CHA-SOLOMON_DAO_LLC_Founding_Charter.md
        - DP-00001_CHA-SOLOMON_DAO_LLC_Operating_Agreement.md
        - DP-00001_ANN-C-rebalancing-state-machine.md

      executed_commit: "bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb"
      executed_tag: "DP-00001@executed-solana-123456789"
      executed_pinned: 2026-01-06T02:10:00Z
      execution_txs:
        - chain: solana
          network: mainnet-beta
          signature: "..."
          slot: 123456999

    result:
      outcome: passed
      for_votes: 12500000
      against_votes: 250000
      abstain_votes: 0
      quorum_reached: true
      notes: null
```

### 4.2 Phase rules (what becomes mandatory when)

- **phase == preformation**: filing is in progress; entity not yet formed.
  No vote fields required; track submission evidence instead.
- **phase == formation**: entity formed/filed; terminal state for DP-00000.
  No vote fields required; track formation evidence instead.
- **phase < voting**: `extensions.dao_proposals.governance.vote.reference` MAY be empty.
- **phase >= voting**: `extensions.dao_proposals.governance.vote.reference` is REQUIRED.
- **phase >= passed**: `extensions.dao_proposals.governance.passed_commit`, `extensions.dao_proposals.governance.passed_tag`,
  `extensions.dao_proposals.governance.passed_pinned`, and `extensions.dao_proposals.governance.adopted_paths` are REQUIRED.
- **phase == executed**: `extensions.dao_proposals.governance.executed_commit`,
  `extensions.dao_proposals.governance.executed_tag`, `extensions.dao_proposals.governance.executed_pinned` are
  REQUIRED (plus `execution_txs` if applicable).

### 4.3 Registry profile and governance extension

The `dao-proposals-v1` registry implementation profile
(`dao-proposals.profile.yaml`) codifies the structural constraints above
in machine-readable form. Governance-specific constraints (annotated tag
requirements, pin fields, adopted-text freeze, vote reference thresholds)
live in the profile's `extensions.governance` block -- not in
`record_constraints` -- per `registry.profile.schema.json`.

The profile MAY also apply META overlay schemas (via `rules.meta_policies.overlay_schema_paths`) to define and validate
registry-specific metadata extension blocks such as `extensions.dao_proposals.*`, while keeping the base META schema permissive.



The DP series is formally registered in `dao-proposals-series.yaml`.

### 4.4 "Passed commit" vs "Executed commit" (and the freeze boundary)

- `passed_*` pins identify the adopted text.
- `adopted_paths` defines the **adopted text surface** (what is
  frozen at `passed_tag`).
- `executed_*` pins identify the repository state when execution
  evidence is finalized.
- `executed_commit` SHOULD equal `passed_commit` **unless** you are only
  adding non-substantive execution artefacts (receipts, tx refs, proof
  links) **outside** `adopted_paths`.
- If you need to change adopted substance (any file in `adopted_paths`),
  that is a **new proposal** (new ID).

### 4.5 Text normalization (MANDATORY for adopted_paths)

Files listed in `extensions.dao_proposals.governance.adopted_paths` are the adopted text surface
frozen at `passed_tag` (see Section 4.4). To keep pinned text stable across
editors/renderers, adopted text MUST avoid "smart punctuation" and
ambiguous characters:

- Quotes: use straight ASCII quotes only: " and ' (no curly quotes).
- Dashes:
  - Use `-` for compounds (e.g. "machine-readable") and list markers.
  - Use `--` (space-dash-dash-space) for parenthetical asides in prose.
  - For ranges, write "to" or "through" (e.g. "§104 to §111") rather
    than an en dash.
- Whitespace: avoid trailing spaces and mixed indentation; do not rely
  on hard-wrapped lines for meaning.

Rendered instruments (PDF/DOCX) may apply typographic punctuation at
render time, but the canonical adopted source text MUST NOT be edited
in-place after it is pinned.

---

## 5. Governance log (`LOG`)

Use the log file to keep a narrative record:

```markdown
# DP-00001 Governance Log

> **Title of the proposed resolution**

---

## Pre-vote Notes

- Rationale adjustments and risk discussions.

---

## Voting Period

- Links to discussion threads and clarifications made during voting.

---

## Post-Execution

- Confirmation of on-chain execution (transaction hashes).
- Deviations between planned and executed sequence, if any.
- Follow-up actions or new proposals required.

```

This keeps debate and context close to the artefacts without polluting
the formal memorandum.

---

## 6. Root index

`INDEX.md` (at the repo root) provides an at-a-glance index of proposals:

Note: this is a **repository index**. Per-record indexes live inside each
proposal directory as `DP-XXXXX_IND-index.md`.


```markdown
# DAO Proposal Index

| ID       | Title                                          | Status       | Directory                          |
| -------- | ---------------------------------------------- | ------------ | ---------------------------------- |
| DP-00000 | Founding Instrument Pack and Formation Filings | formation    | DP-00000-founding-instrument-pack/ |
```

This can be generated automatically from `META.yaml` files.

---

## 7. What is mandatory vs recommended

**Mandatory:**

- `MEM` documents **MUST** include the standard disclaimer footer (see
  `DISCLAIMER.md`).
  **EXCEPT** in the case of a formation pack where a document
  may serves as the Founding Memorandum; which normally carries a
  leading block of statutory notices and disclaimers.
- Adopted proposals MUST be canonically pinned via an **annotated git tag**
  and recorded in `META.yaml` + `LOG-governance.md` (see "Canonical
  pinning on adoption").
- Files in `extensions.dao_proposals.governance.adopted_paths` MUST follow the text normalization
  rules in Section 4.5 (no smart quotes; no en/em dashes).

**Strongly recommended:**

- Follow the directory structure and file naming conventions.
- Prefer explicit links and hashes over prose references.
