# Release Plan

## Current Decision

Status: `BLOCKED — PAYMENT CHARTER, FINANCIAL AUTHORITY, CONTRACT GLUING, AND PUBLICATION EVIDENCE REQUIRED`

The first QSO-PAYMENTS release remains documentation-only. Executable schemas, accounting engines, adapters, credentials, custody, signing, testnet behavior, production settlement, investment products, and return promises remain outside the candidate.

PR #1 now provides a substantial Pages, architecture, A.L.I.S.T.A.I.R.E. integration, obstruction-and-gluing, design-contract, onboarding, security/privacy, operations, recovery, ADR, task-chain, and release-punch-list package. No release is eligible because the portfolio has not approved the payment charter, independent financial authority, Repository `1` role, shared contract owner, identity namespaces, privacy and retention model, exact compatibility witnesses, publication approval, or recovery ownership.

## Versioning

- Scheme: Semantic Versioning after charter, terminology, jurisdictional assumptions, license, privacy model, publication target, subsystem ownership, contract ownership, and review authority are approved.
- First possible documentation candidate: `0.0.1-docs.1`.
- Any later executable candidate must be simulation-only and remain pre-release until contract, arithmetic, replay, privacy, security, revocation, finality, and recovery gates pass.
- Testnet and production require separate versions, separate credentials, independent legal/security review, and explicit human approval.
- No version or page may imply production custody, settlement, investment returns, autonomous transfers, legal certification, jurisdictional approval, or self-authorization by A.L.I.S.T.A.I.R.E.

## Candidate Scope

- Approved purpose, users, terminology, jurisdictions, privacy/data model, license, ecosystem role, review ownership, and prohibited capabilities.
- Approved definition of QSO-PAYMENTS as A.L.I.S.T.A.I.R.E.'s bounded economic-intent, allocation-preview, evidence, dispute, and reconciliation subsystem.
- Explicit separation between Repository `0` proposals, QSO-PAYMENTS validation, independent financial authorization, Repository `1` capability admission, adapter execution, reconciliation, and canonical disposition.
- Documentation-only separation of proposal, intent, validation, authorization, capability, allocation, adapter submission, receipt, pending status, reconciliation, dispute, reversal, custody, and settlement.
- Portfolio obstruction ledger, pairwise gluing contracts, triple-overlap witnesses, result vocabulary, and acceptance order.
- Explicit documentation, simulation, testnet, and production labels.
- Proposed non-executable contract semantics for fixed-precision allocation, idempotency, retries, replay, quote freshness, partial failure, finality limits, correction, revocation, versioning, compatibility, and migration.
- Reproducible MkDocs artifact with exact-source assertion, links, claims, accessibility, security/privacy, workflow-permission, checksum, provenance, publication, and rollback evidence.

## Selected Completed Candidate Work

No release task is selected as complete. Candidate documentation work includes:

- expanded repository and Pages overview;
- project guide, architecture, lifecycle, trust-boundary, and repository-dependency documentation;
- A.L.I.S.T.A.I.R.E. context, resource lifecycle, capability matrix, autonomous-evolution constraints, and unresolved ownership ledger;
- portfolio obstruction and gluing analysis with 18 active incompatibilities;
- eight pairwise contract edges and six required triple-overlap witnesses;
- design contracts, developer onboarding, security/privacy, operations, incident response, recovery, and ADR documentation;
- pinned documentation dependencies and strict exact-head validation workflow;
- retained site, source-identity, and SHA-256 evidence artifacts for the prior candidate head;
- expanded task chain and evidence-oriented punch list.

These are inputs to review. They do not prove the charter, contract, authority, publication, simulation, testnet, or production gates passed.

## Working Route

```text
Repository 0 local resource proposal
→ QSO-PAYMENTS validated economic intent
→ approved review surface
→ independent financial authorization
→ Repository 1 narrow capability admission
→ disabled external adapter
→ execution evidence
→ QSO-PAYMENTS reconciliation
→ Repository 1 canonical disposition
```

This route is not operational. Repository `1` cannot create financial approval by implication. QSO-PAYMENTS cannot approve or fund its own intent. An interface cannot create authority merely by displaying or transmitting a decision. Adapter success does not establish canonical or legal finality.

## Acceptance Gates

| Gate | Status | Requirement |
|---|---|---|
| Charter/payment boundary | BLOCKED | Approve purpose, users, terminology, jurisdictions, privacy/license model, subsystem role, environment model, review ownership, and prohibited production capabilities. |
| Financial authority | BLOCKED | Name the independent financial approver and revoker; define authentication, scope, expiry, jurisdictional assumptions, and human accountability. |
| Repository `1` role | BLOCKED | Approve or replace Repository `1` as generic capability and canonical-disposition authority after financial approval; prohibit authority broadening. |
| Contract ownership | BLOCKED | Designate the canonical owner of intent, authorization, capability, receipt, dispute, reconciliation, correction, revocation, and identity schemas. |
| Gluing witnesses | DOCUMENTED / UNVERIFIED | Accept the obstruction ledger, pairwise edges, triple-overlap witnesses, shared status vocabulary, and machine-readable fixture plan. |
| Task completion | BLOCKED | Required task-chain items are `DONE`; `punchlist.md` contains linked evidence for every included gate. |
| Publication/deployment | NOT AUTHORIZED | A separate decision authorizes Pages publication, then exact URL, deployed commit, content checks, and rollback evidence are retained. |
| Links/build | PRIOR EXACT-HEAD EVIDENCE | Pinned dependencies, submitted-head assertion, strict build, and artifact hashing passed at the previous head; the updated head requires a fresh accepted run. |
| Claims/legal | PARTIAL | Boundaries and disclaimers exist; payment, jurisdiction, tax, finality, autonomous-development, and economic claims require independent review. |
| Accessibility | PARTIAL | Site semantics and presentation are designed; exact artifact testing and retained results remain pending. |
| Security/privacy | PARTIAL | Threats, secret prohibitions, data minimization, separation of duties, workflow controls, incident triggers, and recovery are documented; independent review and exercises remain pending. |
| Provenance | CANDIDATE | Exact-source identity and SHA-256 evidence are generated by the workflow; a fresh accepted run and approval record remain required. |
| Approval | PENDING | Explicit release approval after every included-scope gate passes. |

## Artifact Requirements

- Approved payment-boundary charter and A.L.I.S.T.A.I.R.E. subsystem placement.
- Financial authority, generic capability authority, credential/custody, incident, emergency-stop, recovery, and release ownership record.
- Approved schema/package owner, identity namespaces, compatibility policy, and migration plan.
- Accepted obstruction ledger and gluing-witness specification.
- Reproducible static-site bundle and source archive.
- Source-identity record and SHA-256 manifest tied to the immutable candidate.
- Link, accessibility, claims/legal, security/privacy, workflow-permission, and content-review reports.
- Publication/provenance record, deployed-commit verification, and documentation rollback evidence if Pages publication is approved.
- Any later simulation candidate additionally requires versioned schemas, identical cross-repository fixtures, fixed-precision accounting and reconciliation tests, quote freshness, replay and partial-failure tests, revocation and correction propagation, recovery evidence, and SBOM where applicable.

## Rollback Criteria

Withdraw or roll back if content implies production settlement, custody, guaranteed returns, autonomous transfers, self-authorization, legal certification, or jurisdictional approval; financial approval and generic capability semantics are ambiguous; environment labels mislead; identity, amount, precision, quote, replay, privacy, finality, correction, or recovery rules conflict; links or builds fail; sensitive data is exposed; accessibility blocks use; publication is non-reproducible; severe security/privacy findings remain; workflow provenance is incomplete; or artifact hashes differ.

Restore the previous verified source or Pages artifact, preserve rejected reports and hashes, revoke any affected publication or future adapter capability, and retain the incident and recovery record.

## Unresolved Blockers

- Payment charter, terminology, jurisdictional assumptions, privacy/license model, ecosystem role, reviewer ownership, and prohibited-capability boundary require approval.
- Independent financial approval and revocation ownership are not designated.
- Repository `1`'s exact role in capability admission and canonical disposition is not approved.
- Shared schema/package ownership and identity namespaces are unresolved.
- Amount, precision, fee, tax, quote, replay, finality, correction, privacy, retention, and recovery semantics lack accepted machine-readable fixtures.
- Adapter credential, signing, custody, monitoring, incident, emergency-stop, and recovery topology is not approved.
- The updated exact head requires fresh strict-build and retained-artifact evidence.
- Publication, accessibility, claims/legal, independent security/privacy, and exercised rollback evidence remain pending.
- Settlement-adapter descriptions remain documentation-only and cannot be represented as executable capability.

## Release Log

- 2026-07-16: Aligned the candidate with the documentation-only payment-boundary directive; release remained blocked by charter approval and publication evidence.
- 2026-07-19: PR #1 established a substantial MkDocs documentation and operations package plus a release punch list; no gate was marked complete.
- 2026-07-20: Added the A.L.I.S.T.A.I.R.E. subsystem boundary, autonomous-development separation of duties, capability matrix, and exact-source documentation evidence workflow.
- 2026-07-21: Added the portfolio obstruction and gluing analysis, clarified the Repository `0` → QSO-PAYMENTS → financial authorization → Repository `1` route, and expanded release gates for schema ownership, finality, revocation, compatibility, and recovery. Release remains blocked and no financial authority was activated.
