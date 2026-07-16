# Release Plan

## Current Decision

Status: `BLOCKED — PAYMENT CHARTER AND PUBLICATION EVIDENCE REQUIRED`

The first QSO-PAYMENTS release is now explicitly documentation-only; executable schemas, adapters, custody, signing, and settlement remain outside the candidate. No release is eligible because P0 is blocked on approval of the payment-boundary charter, `punchlist.md` is absent, and candidate head `94d33e6d3d46f04bfde425bfd65ea3572a373c33` lacks current Pages deployment, link/HTML, accessibility, claim, security/privacy, checksum, provenance, and rollback evidence.

## Versioning

- Scheme: Semantic Versioning after charter, terminology, jurisdictional assumptions, license, privacy model, and publication target are approved.
- First possible documentation candidate: `0.0.1-docs.1`.
- Any later executable candidate must be simulation-only and remain pre-release until contract/accounting/security gates pass.
- No version or page may imply production custody, settlement, investment returns, or autonomous transfers.

## Release Scope

- Approved purpose, users, terminology, jurisdictions, privacy/data model, license, ecosystem role, and prohibited capabilities.
- Documentation-only separation of intent, authorization, allocation, receipt, dispute, escrow milestones, custody, adapters, and settlement.
- Explicit simulation/testnet/production labels.
- Reproducible static-site artifact with link, HTML, accessibility, claim, security/privacy, workflow-permission, checksum, provenance, and rollback evidence.

## Selected Completed Work

None selected. The README, Pages site, styles, and deployment workflow are candidate inputs, but no approved task or retained publication evidence establishes a releasable snapshot.

## Planned Changelog Entries

- `Documentation`: approved payment charter, terminology, environment model, non-goals, jurisdictional assumptions, and ecosystem boundary.
- `Changed`: evidence-classified capability wording and explicit docs/simulation/testnet/production separation.
- `Security`: authorization, custody, credentials, privacy, external links, workflow permissions, and supply-chain review.
- `Accessibility`: navigation, semantics, keyboard path, contrast, scaling, and notice readability.
- `Release`: reproducible site/source artifact, reports, checksums, provenance, and approval.

## Acceptance Gates

| Gate | Status | Requirement |
|---|---|---|
| Charter/payment boundary | BLOCKED | Approve purpose, users, terminology, jurisdictions, privacy/license model, and prohibited production capabilities. |
| Task completion | FAIL | P0 and P1 are `DONE`; `punchlist.md` exists with linked evidence. |
| Publication/deployment | NO CURRENT EVIDENCE | Pages workflow succeeds at the immutable candidate commit and artifact/URL are retained. |
| Links/HTML/build | NO EVIDENCE | Links, HTML/CSS, metadata, responsive behavior, and reproducible bundle pass. |
| Claims/compliance | PARTIAL | Disclaimers exist; every payment, route, adapter, environment, and economic claim is evidence-classified and reviewed. |
| Accessibility | NO EVIDENCE | Semantics, keyboard/focus, contrast, scaling, and notice presentation pass. |
| Security/privacy | NO EVIDENCE | No credentials/custody/transfers; secret, dependency, workflow, external-link, content, privacy, and supply-chain checks pass. |
| Documentation | PARTIAL | Site exists; approved charter, exact publication commands, limitations, assumptions, operations, and rollback are incomplete. |
| Provenance | NO EVIDENCE | Commit, workflow run, tool/action versions, commands, artifact hashes, repository URL, and attestations are retained. |
| Approval | PENDING | Explicit release approval after all included-scope gates pass. |

## Artifact Requirements

- Approved payment-boundary charter, threat/compliance assumptions, and capability-claim inventory.
- Reproducible static-site bundle and source archive.
- Link, HTML, accessibility, claims, security/privacy, and workflow-permission reports.
- SHA-256 checksum manifest, publication/provenance record, and rollback artifact.
- Any later simulation candidate additionally requires versioned schemas, deterministic fixtures, accounting/reconciliation tests, and SBOM where applicable.

## Rollback Criteria

Withdraw or roll back if content implies production settlement, custody, guaranteed returns, or autonomous transfers; authorization semantics are ambiguous; environment labels mislead; links or deployment fail; sensitive data is exposed; accessibility blocks use; publication is non-reproducible; severe security/compliance findings remain; or hashes differ. Restore the previous verified Pages artifact/tag and preserve rejected reports and hashes.

## Unresolved Blockers

- Approval is required for the payment charter, terminology, jurisdictional assumptions, privacy/license model, ecosystem role, and prohibited-capability boundary.
- P0 is blocked; `punchlist.md` and accepted publication evidence are absent.
- No current Pages run, site artifact, link/HTML check, accessibility report, claim review, security/privacy report, checksum, provenance, or rollback evidence exists.
- Settlement-adapter and economic-route descriptions remain documentation-only and cannot be represented as executable capability.

## Release Log

- 2026-07-16: Aligned the candidate with the documentation-only payment-boundary directive; release remains blocked by charter approval and publication evidence.