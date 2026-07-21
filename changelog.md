# Changelog

## Unreleased

### Product
- 2026-07-16 — Established a documentation-only first product for payment intent, authorization, allocation, receipts, disputes, adapters, custody, and settlement boundaries.
- 2026-07-16 — Blocked executable simulation work pending approval of terminology, jurisdictions, privacy, license, compliance assumptions, and prohibited production capabilities.
- 2026-07-20 — Defined QSO-PAYMENTS as A.L.I.S.T.A.I.R.E.'s bounded economic-intent and evidence subsystem rather than the autonomous-development or financial-authority control plane.
- 2026-07-21 — Refined the subsystem role to economic intent, allocation preview, evidence, dispute, and reconciliation; preserved financial approval, capability issuance, custody, and settlement as independent responsibilities.

### Architecture
- Intent and policy remain separate from authorization, capability admission, custody, adapter execution, reconciliation, canonical disposition, and settlement; future adapters are disabled and out of the first release.
- 2026-07-19 — Added a documented authority model, record lifecycle, environment classification, data classification, adapter boundary, invariants, and repository dependency rules without enabling executable payment behavior.
- 2026-07-19 — Added proposed record-envelope, authorization, fixed-precision allocation, idempotency, retry, partial-failure, receipt, compatibility, and migration contracts; all remain non-executable design guidance.
- 2026-07-19 — Recorded ADR-0001 proposing a documentation-only first release and listing the approvals required before simulation work.
- 2026-07-20 — Added an A.L.I.S.T.A.I.R.E. portfolio diagram, autonomous resource lifecycle, capability and authority matrix, cross-repository interface rules, failure-containment controls, and ownership-decision ledger.
- 2026-07-20 — Made self-approval, inherited financial authority, silent environment escalation, and cross-repository credential inheritance explicit architectural prohibitions.
- 2026-07-21 — Added an obstruction and gluing analysis with 18 active compatibility failures, eight pairwise contract edges, six triple-overlap witness groups, explicit result semantics, and an acceptance order.
- 2026-07-21 — Documented the lowest-coupling route as Repository `0` proposal → QSO-PAYMENTS intent → independent financial authorization → Repository `1` narrow capability → disabled adapter → evidence → reconciliation → canonical disposition.
- 2026-07-21 — Clarified that Repository `1` cannot create financial approval by implication and that adapter execution cannot force canonical or legal finality.

### Documentation
- 2026-07-19 — Added a project guide and architecture reference covering purpose, onboarding, contract families, threat model, release gates, and rollback boundaries.
- 2026-07-19 — Added dedicated design-contract, onboarding, security/privacy, operations/recovery, and architecture-decision pages.
- 2026-07-19 — Replaced the single static landing page with a navigable MkDocs site and expanded the README documentation map.
- 2026-07-20 — Added a dedicated A.L.I.S.T.A.I.R.E. integration guide and reconciled the README, project guide, architecture, Pages navigation, task chain, release plan, punch list, and changelog around the canonical system objective.
- 2026-07-21 — Added the obstruction and gluing page to MkDocs navigation and aligned README, task chain, punch list, release plan, and changelog with the current Repository `0`/`1` portfolio model.

### Accessibility
- 2026-07-19 — Added visible keyboard focus, reduced-motion behavior, readable responsive tables, semantic navigation, and warning presentation that does not rely on color alone.
- 2026-07-21 — Required authority, environment, result, and finality distinctions to remain understandable without diagrams or color alone.

### Security
- 2026-07-19 — Documented secret prohibitions, payment-metadata minimization, adapter-substitution and receipt risks, claims controls, workflow least privilege, incident triggers, and evidence-preserving recovery.
- 2026-07-20 — Documented separation between autonomous-development orchestration, independent financial authorization, adapter credentials, and emergency-disable ownership.
- 2026-07-20 — Hardened the documentation workflow to check out and assert the submitted pull-request head, isolate deployment permissions, generate a SHA-256 manifest, and retain reviewable source/build evidence.
- 2026-07-21 — Added threats and required witnesses for financial-approval/capability confusion, identity mismatch, stale quotes, replay, duplicate effects, false finality, privacy leakage, automated budget escalation, correction, revocation, emergency stop, and recovery.

### Implementation
- The repository remains documentation-only; no executable payment schema, accounting engine, credential, custody, signing, adapter, testnet behavior, or production transfer path was added.
- 2026-07-19 — Pinned MkDocs 1.6.1 and updated the validation workflow to run `mkdocs build --strict` and retain exact-source evidence.
- 2026-07-21 — No runtime or schema implementation changed; all new contract, route, and fixture material is documentation-only.

### Release
- The documentation candidate remains blocked until charter and portfolio authority decisions, contract ownership, compatibility witnesses, reproducible publication, claims/accessibility/security review, checksums, provenance, and rollback evidence pass.
- 2026-07-19 — Documentation content advanced substantially, but no release gate was marked complete and no production capability was inferred.
- 2026-07-20 — Exact-source and checksum evidence generation became part of the candidate workflow; accepted exact-head results and all human review gates remain required.
- 2026-07-21 — Expanded release gates to require independent financial-authority ownership, Repository `1` role approval, machine-readable gluing fixtures, finality and correction semantics, and a cross-repository emergency-stop and recovery exercise.

### Deployment
- Pages is the only proposed deployment surface; no credentialed, testnet, or production payment deployment is authorized.
- 2026-07-19 — The Pages source builds into `site/`; publication remains separately governed and does not constitute payment-release approval.
- 2026-07-20 — Pull-request validation retained read-only permissions and produced review artifacts without publishing.
- 2026-07-21 — The documentation changes do not authorize Pages publication; the updated exact head requires a fresh accepted validation artifact before review.

## Entry Format
- Date
- Category: Product / Architecture / Added / Changed / Fixed / Security / Release / Deployment
- Summary
- Evidence: issue, PR, commit, workflow, artifact, or deployment record
- Impact and migration notes where applicable
