# Changelog

## Unreleased

### Product
- 2026-07-16 — Established a documentation-only first product for payment intent, authorization, allocation, receipts, disputes, adapters, custody, and settlement boundaries.
- 2026-07-16 — Blocked executable simulation work pending approval of terminology, jurisdictions, privacy, license, compliance assumptions, and prohibited production capabilities.
- 2026-07-20 — Defined QSO-PAYMENTS as A.L.I.S.T.A.I.R.E.'s bounded economic-intent and evidence subsystem rather than the autonomous-development or financial-authority control plane.

### Architecture
- Intent and policy remain separate from authorization, custody, adapter execution, and settlement; future adapters are disabled and out of the first release.
- 2026-07-19 — Added a documented authority model, record lifecycle, environment classification, data classification, adapter boundary, invariants, and repository dependency rules without enabling executable payment behavior.
- 2026-07-19 — Added proposed record-envelope, authorization, fixed-precision allocation, idempotency, retry, partial-failure, receipt, compatibility, and migration contracts; all remain non-executable design guidance.
- 2026-07-19 — Recorded ADR-0001 proposing a documentation-only first release and listing the approvals required before simulation work.
- 2026-07-20 — Added an A.L.I.S.T.A.I.R.E. portfolio diagram, autonomous resource lifecycle, capability and authority matrix, cross-repository interface rules, failure-containment controls, and ownership-decision ledger.
- 2026-07-20 — Made self-approval, inherited financial authority, silent environment escalation, and cross-repository credential inheritance explicit architectural prohibitions.

### Documentation
- 2026-07-19 — Added a project guide and architecture reference covering purpose, onboarding, contract families, threat model, release gates, and rollback boundaries.
- 2026-07-19 — Added dedicated design-contract, onboarding, security/privacy, operations/recovery, and architecture-decision pages.
- 2026-07-19 — Replaced the single static landing page with a navigable MkDocs site and expanded the README documentation map.
- 2026-07-20 — Added a dedicated A.L.I.S.T.A.I.R.E. integration guide and reconciled the README, project guide, architecture, Pages navigation, task chain, release plan, punch list, and changelog around the canonical system objective.

### Accessibility
- 2026-07-19 — Added visible keyboard focus, reduced-motion behavior, readable responsive tables, semantic navigation, and warning presentation that does not rely on color alone.

### Security
- 2026-07-19 — Documented secret prohibitions, payment-metadata minimization, adapter-substitution and receipt risks, claims controls, workflow least privilege, incident triggers, and evidence-preserving recovery.
- 2026-07-20 — Documented separation between autonomous-development orchestration, independent financial authorization, adapter credentials, and emergency-disable ownership.
- 2026-07-20 — Hardened the documentation workflow to check out and assert the submitted pull-request head, isolate deployment permissions, generate a SHA-256 manifest, and retain reviewable source/build evidence.

### Implementation
- The repository remains documentation-only; no executable payment schema, accounting engine, credential, custody, signing, adapter, testnet behavior, or production transfer path was added.
- 2026-07-19 — Pinned MkDocs 1.6.1 and updated the Pages workflow to run `mkdocs build --strict` on documentation pull requests before deployment from `main`.

### Release
- The documentation candidate remains blocked until charter and portfolio authority decisions, reproducible deployment, claims/accessibility/security review, checksums, provenance, and rollback evidence pass.
- 2026-07-19 — Documentation content advanced substantially, but no release gate was marked complete and no production capability was inferred.
- 2026-07-20 — Exact-source and checksum evidence generation became part of the candidate workflow; accepted exact-head results and all human review gates remain required.

### Deployment
- Pages is the only proposed deployment surface; no credentialed, testnet, or production payment deployment is authorized.
- 2026-07-19 — The Pages source now builds into `site/`; deployment still occurs only after merge to `main` and does not itself constitute release approval.
- 2026-07-20 — Pages deployment permissions were moved to the deploy job while pull-request builds retain only read access and produce review artifacts without publishing.

## Entry Format
- Date
- Category: Product / Architecture / Added / Changed / Fixed / Security / Release / Deployment
- Summary
- Evidence: issue, PR, commit, workflow, artifact, or deployment record
- Impact and migration notes where applicable
