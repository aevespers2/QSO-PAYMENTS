# Changelog

## Unreleased

### Product
- 2026-07-16 — Established a documentation-only first product for payment intent, authorization, allocation, receipts, disputes, adapters, custody, and settlement boundaries.
- 2026-07-16 — Blocked executable simulation work pending approval of terminology, jurisdictions, privacy, license, compliance assumptions, and prohibited production capabilities.

### Architecture
- Intent and policy remain separate from authorization, custody, adapter execution, and settlement; future adapters are disabled and out of the first release.
- 2026-07-19 — Added a documented authority model, record lifecycle, environment classification, data classification, adapter boundary, invariants, and repository dependency rules without enabling executable payment behavior.
- 2026-07-19 — Added proposed record-envelope, authorization, fixed-precision allocation, idempotency, retry, partial-failure, receipt, compatibility, and migration contracts; all remain non-executable design guidance.
- 2026-07-19 — Recorded ADR-0001 proposing a documentation-only first release and listing the approvals required before simulation work.

### Documentation
- 2026-07-19 — Added a project guide and architecture reference covering purpose, onboarding, contract families, threat model, release gates, and rollback boundaries.
- 2026-07-19 — Added dedicated design-contract, onboarding, security/privacy, operations/recovery, and architecture-decision pages.
- 2026-07-19 — Replaced the single static landing page with a navigable MkDocs site and expanded the README documentation map.

### Accessibility
- 2026-07-19 — Added visible keyboard focus, reduced-motion behavior, readable responsive tables, semantic navigation, and warning presentation that does not rely on color alone.

### Security
- 2026-07-19 — Documented secret prohibitions, payment-metadata minimization, adapter-substitution and receipt risks, claims controls, workflow least privilege, incident triggers, and evidence-preserving recovery.

### Implementation
- The repository remains documentation-only; no executable payment schema, accounting engine, credential, custody, signing, adapter, testnet behavior, or production transfer path was added.
- 2026-07-19 — Pinned MkDocs 1.6.1 and updated the Pages workflow to run `mkdocs build --strict` on documentation pull requests before deployment from `main`.

### Release
- The documentation candidate remains blocked until charter approval, reproducible deployment, claims/accessibility/security review, checksums, provenance, and rollback evidence pass.
- 2026-07-19 — Documentation content advanced substantially, but no release gate was marked complete and no production capability was inferred.

### Deployment
- Pages is the only proposed deployment surface; no credentialed, testnet, or production payment deployment is authorized.
- 2026-07-19 — The Pages source now builds into `site/`; deployment still occurs only after merge to `main` and does not itself constitute release approval.

## Entry Format
- Date
- Category: Product / Architecture / Added / Changed / Fixed / Security / Release / Deployment
- Summary
- Evidence: issue, PR, commit, workflow, artifact, or deployment record
- Impact and migration notes where applicable
