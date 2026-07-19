# Release Plan

## Current Decision

Status: `BLOCKED — PAYMENT CHARTER, EXACT-HEAD REVIEW, AND PUBLICATION EVIDENCE REQUIRED`

The first QSO-PAYMENTS release is explicitly documentation-only; executable schemas, accounting engines, adapters, custody, signing, testnet behavior, production settlement, investment products, and return promises remain outside the candidate. PR #1 now provides a substantial Pages, architecture, design-contract, onboarding, security/privacy, operations, rollback, ADR, and release-punch-list package, but no release is eligible because P0 remains blocked and the exact PR head lacks retained claims, accessibility, security/privacy, link/HTML, artifact, checksum, provenance, deployment, and rollback evidence.

## Versioning

- Scheme: Semantic Versioning after charter, terminology, jurisdictional assumptions, license, privacy model, and publication target are approved.
- First possible documentation candidate: `0.0.1-docs.1`.
- Any later executable candidate must be simulation-only and remain pre-release until contract, arithmetic, replay, privacy, security, and recovery gates pass.
- No version or page may imply production custody, settlement, investment returns, autonomous transfers, legal certification, or jurisdictional approval.

## Release Scope

- Approved purpose, users, terminology, jurisdictions, privacy/data model, license, ecosystem role, review ownership, and prohibited capabilities.
- Documentation-only separation of proposal, intent, validation, authorization, allocation, adapter submission, receipt, reconciliation, dispute, custody, and settlement.
- Explicit documentation, simulation, testnet, and production labels.
- Proposed non-executable contract semantics for fixed-precision allocation, idempotency, retries, partial failure, finality limits, versioning, compatibility, and migration.
- Reproducible MkDocs Pages artifact with link, HTML, accessibility, claims, security/privacy, workflow-permission, checksum, provenance, deployment, and rollback evidence.

## Selected Completed Work

No release task is selected as complete. Candidate documentation work now includes:

- expanded repository and Pages overview;
- project guide, architecture, lifecycle, trust-boundary, and repository-dependency documentation;
- design contracts, developer onboarding, security/privacy, operations, incident-response, recovery, and ADR documentation;
- pinned MkDocs dependency and strict pull-request build workflow;
- an evidence-oriented `punchlist.md`.

These are inputs to P0/P1 review, not proof that either gate passed.

## Planned Changelog Entries

- `Documentation`: approved payment charter, terminology, environment model, non-goals, jurisdictional assumptions, ecosystem boundary, and reviewer ownership.
- `Changed`: evidence-classified capability wording and explicit documentation/simulation/testnet/production separation.
- `Security`: authorization, custody, credentials, privacy, external links, workflow permissions, supply chain, and incident response.
- `Accessibility`: navigation, semantics, keyboard path, contrast, scaling, reflow, and warning readability.
- `Release`: reproducible site/source artifact, reports, checksums, provenance, deployment verification, rollback evidence, and approval.

## Acceptance Gates

| Gate | Status | Requirement |
|---|---|---|
| Charter/payment boundary | BLOCKED | Approve purpose, users, terminology, jurisdictions, privacy/license model, ecosystem role, review ownership, and prohibited production capabilities. |
| Task completion | BLOCKED | P0 and P1 are `DONE`; `punchlist.md` contains linked evidence for every included gate. |
| Publication/deployment | NO CURRENT EVIDENCE | Pages workflow succeeds at the immutable candidate commit and artifact, URL, deployed commit, and post-deployment checks are retained. |
| Links/HTML/build | CANDIDATE WORKFLOW ADDED | Pinned dependencies and `mkdocs build --strict` exist; exact-head result, link/HTML validation, metadata, responsive behavior, and reproducibility evidence remain pending. |
| Claims/compliance | PARTIAL | Boundaries and disclaimers are documented; every payment, route, adapter, environment, finality, and economic claim still requires independent review. |
| Accessibility | PARTIAL | Keyboard focus, reduced motion, responsive tables, and semantic structure are designed; exact artifact testing and retained results remain pending. |
| Security/privacy | PARTIAL | Threats, secret prohibitions, data minimization, workflow controls, and incident triggers are documented; scans and independent review remain pending. |
| Documentation | SUBSTANTIAL CANDIDATE | Overview, architecture, design, onboarding, security/privacy, operations, ADR, and rollback content exist; charter approval and human review remain pending. |
| Provenance | NO CURRENT EVIDENCE | Commit, workflow run, tool/action versions, commands, artifact hashes, repository URL, and attestations are retained. |
| Approval | PENDING | Explicit release approval after all included-scope gates pass. |

## Artifact Requirements

- Approved payment-boundary charter, threat/compliance assumptions, review ownership, and capability-claim inventory.
- Reproducible static-site bundle and source archive.
- Link, HTML, accessibility, claims, security/privacy, and workflow-permission reports.
- SHA-256 checksum manifest, publication/provenance record, deployed-commit verification, and rollback artifact.
- Any later simulation candidate additionally requires versioned schemas, deterministic fixtures, fixed-precision accounting and reconciliation tests, replay and partial-failure tests, compatibility fixtures, and SBOM where applicable.

## Rollback Criteria

Withdraw or roll back if content implies production settlement, custody, guaranteed returns, autonomous transfers, legal certification, or jurisdictional approval; authorization semantics are ambiguous; environment labels mislead; links or deployment fail; sensitive data is exposed; accessibility blocks use; publication is non-reproducible; severe security/privacy findings remain; workflow provenance is incomplete; or artifact hashes differ. Restore the previous verified Pages artifact or source commit and preserve rejected reports, artifacts, and hashes.

## Unresolved Blockers

- Approval is required for the payment charter, terminology, jurisdictional assumptions, privacy/license model, ecosystem role, reviewer ownership, and prohibited-capability boundary.
- P0 is blocked; P1 cannot be completed until P0 and all exact-head publication evidence are satisfied.
- `punchlist.md` exists, but all evidence links and approvals remain pending.
- No accepted Pages deployment, link/HTML report, accessibility report, claim review, security/privacy report, checksum, provenance record, or exercised rollback evidence exists for the current PR head.
- Settlement-adapter and economic-route descriptions remain documentation-only and cannot be represented as executable capability.

## Release Log

- 2026-07-16: Aligned the candidate with the documentation-only payment-boundary directive; release remained blocked by charter approval and publication evidence.
- 2026-07-19: PR #1 established a substantial MkDocs documentation and operations package plus a release punch list; no gate was marked complete and release remains blocked.
