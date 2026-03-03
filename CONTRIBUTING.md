# Contributing - DAO proposals

This repository is a publication / coordination venue for governance
materials.
See `DISCLAIMER.md` and `LICENSE`.

By submitting a Contribution (as defined in LICENSE Section 7), you agree to
the contribution terms in the LICENSE, including the grant-back to the DAO.
Repository Materials are Protocol IP.

## Proposal lifecycle hygiene

- Draft proposals can be submitted by anyone (subject to repo controls).
- The canonical "what the DAO adopted" is the DAO's governance record
  (on-chain and any executed/ filed instruments). This repository is used
to make the adopted text auditable and precisely referenceable.

## Mandatory requirements

1. **MEM footer**  
   All `*_MEM-*.md` files MUST include the standard disclaimer footer
   (see `DISCLAIMER.md`).

2. **Canonical pinning on adoption**  
   Any proposal that is adopted (`status.phase` = `passed` or later) MUST
   be pinned to an **annotated git tag** that includes the vote/tx reference
   and the commit hash, and MUST be recorded in `META.yaml` and
   `LOG-governance.md`.

3. **No in-place edits after adoption**  
   After adoption, the adopted text is immutable for audit purposes.
   Corrections/amendments require a new proposal ID that `supersedes`
   the prior proposal.

## Metadata (`META.yaml`) requirements on adoption

`META.yaml` MUST include (names may be adapted, but the data must exist):

Voting / discussion (once applicable):
- `governance.system`
- `governance.discussion_urls` (or a single discussion URL)
- `governance.vote.reference` (e.g. `MetaDAO#123`) **(REQUIRED once phase
  >= voting)**
- `governance.vote.tx_refs` (if there is a vote tx)

Canonical pins (multi-stage):
- `governance.passed_commit` **(REQUIRED once phase >= passed)**
- `governance.passed_tag` **(REQUIRED once phase >= passed)**
- `governance.passed_pinned` **(REQUIRED once phase >= passed)**

Freeze surface (hard-nosed rule):
- `governance.adopted_paths` **(REQUIRED once phase >= passed)** - list of
  repository paths that constitute the adopted text surface.

Execution (only when applicable):
- `governance.executed_commit` **(REQUIRED once phase == executed)**
- `governance.executed_tag` **(REQUIRED once phase == executed)**
- `governance.executed_pinned` **(REQUIRED once phase == executed)**
- `governance.execution_txs` (list, REQUIRED if the proposal has execution
  txs)

Substantive freeze rule:
- After the **passed_tag** is created, any substantive change to any file
  in `governance.adopted_paths` requires a **new proposal ID**.
- The **executed_commit** may add execution artefacts only (links/receipts/
  tx refs/proof material), and SHOULD do so outside
  `governance.adopted_paths`.

## Governance log (`LOG-governance.md`) requirements

`LOG-governance.md` is append-only. Each event entry should capture:

- timestamp (UTC)
- event type (`draft_created`, `submitted`, `voting_started`, `passed`,
  `executed`, `superseded`, etc.)
- links (discussion, vote page)
- tx references (vote tx / execution tx)
- canonical pin (commit + tag) when passed/executed

## Annotated tag requirements

Use **annotated tags** (`git tag -a`). Tags are the legal-grade "pins"
that make the adopted text and its execution evidence trivially provable.

You MUST create:

- **Passed tag** (once the proposal is adopted / ratified): points to
  the adopted commit, and freezes `governance.adopted_paths`.
- **Executed tag** (once execution evidence is finalized): points to the
  executed commit (often the same commit; may differ only to add
  non-substantive execution artefacts **outside**
  `governance.adopted_paths`).

The tag message MUST include:

- proposal ID
- vote reference + outcome (for passed tag)
- vote tx (if present)
- execution tx(s) (for executed tag, if present)
- the pinned commit hash (include it in the message even though the tag
 points to it)

Recommended tag names:

- `DP-00001@passed-MetaDAO-123`
- `DP-00001@executed-solana-<slot>` (or `DP-00001@executed-YYYY-MM-DD`)
