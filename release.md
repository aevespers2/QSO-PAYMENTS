# Release Plan

## Current decision

Status: `BLOCKED — PAYMENT CHARTER, INDEPENDENT FINANCIAL AUTHORITY, CONTRACT OWNERSHIP, ACCESSIBILITY REVIEW, AND PUBLICATION EVIDENCE REQUIRED`

The first QSO-PAYMENTS release remains documentation-only. Executable schemas, accounting engines, adapters, credentials, custody, signing, testnet behavior, production settlement, investment products, device control, remote administration, and return promises remain outside the candidate.

PR #1 provides a Pages, architecture, A.L.I.S.T.A.I.R.E. integration, portable-trust/financial-authority, obstruction-and-gluing, design-contract, conceptual contract-reference, accessibility/plain-language, onboarding, security/privacy, operations, recovery, ADR, task-chain, and release-punch-list package. The current focused milestone adds a decision-ready **independent financial-authorization review protocol** while preserving `DOCUMENTED_NOT_AUTHORIZED` as the governing status.

No release is eligible because the portfolio has not approved the payment charter, independent authorizer and authority source, Repository `1` role, device/workspace identity model, shared contract owner, privacy and retention model, exact compatibility witnesses, rendered accessibility review, publication approval, correction/revocation propagation, or recovery ownership.

## Versioning

- Scheme: Semantic Versioning after charter, terminology, jurisdictional assumptions, license, privacy model, publication target, subsystem ownership, device/workspace identity, contract ownership, financial authority, and review ownership are approved.
- First possible documentation candidate: `0.0.1-docs.1`.
- Any later executable candidate must be simulation-only and remain pre-release until contract, arithmetic, device binding, replay, privacy, security, revocation, finality, accessibility, and recovery gates pass.
- Testnet and production require separate versions, separate credentials, independent legal/security review, trusted-device and workspace controls, and explicit human approval.
- No version or page may imply production custody, settlement, investment returns, autonomous transfers, device-control authority, legal certification, jurisdictional approval, or self-authorization by A.L.I.S.T.A.I.R.E.

## Candidate scope

- Approved purpose, users, terminology, jurisdictions, privacy/data model, license, ecosystem role, review ownership, and prohibited capabilities.
- Approved definition of QSO-PAYMENTS as A.L.I.S.T.A.I.R.E.'s bounded economic-intent, allocation-preview, evidence, dispute, and reconciliation subsystem.
- Explicit separation between Repository `0` proposals and device observations, QSO-PAYMENTS validation, independent financial review and authorization, Repository `1` device/workspace verification and capability admission, adapter execution, reconciliation, and canonical disposition.
- Portable trust and financial-authority profile covering device enrollment, ownership scope, workspace/source identity, wrong-device rejection, loss, theft, replacement, revocation, privacy, cache invalidation, emergency stop, and recovery.
- Conceptual contract and interface reference covering surfaces, envelope, record families, text status vocabulary, candidate reason-code classes, migration requirements, and explicit non-executable examples.
- Independent financial-authorization review guide covering role separation, authority source, exact intent and scope bindings, conflicts, evidence classes, decision states, material-change rules, fail-closed stops, correction, revocation, dispute, downstream notification, retention, accessibility, and reviewer onboarding.
- Accessibility and plain-language guidance covering text-equivalent authority states, diagram prose, tables, links, code examples, keyboard navigation, zoom, reflow, motion, and comprehension.
- Portfolio obstruction ledger, pairwise gluing contracts, triple-overlap witnesses, result vocabulary, and acceptance order.
- Explicit documentation, simulation, testnet, and production labels.
- Proposed non-executable semantics for fixed-precision allocation, idempotency, retries, replay, quote freshness, device/workspace binding, partial failure, finality limits, correction, revocation, versioning, compatibility, migration, and rollback.
- Reproducible MkDocs artifact with exact-source assertion, links, claims, accessibility, security/privacy, workflow-permission, checksum, provenance, publication, and rollback evidence.

## Completed candidate documentation

No release gate is complete. Candidate review inputs now include:

- project and Pages overviews;
- architecture, lifecycle, trust-boundary, repository-dependency, and A.L.I.S.T.A.I.R.E. integration documentation;
- portable trust and financial-authority boundary with separate subject identities, trust states, loss/theft behavior, wrong-device and wrong-workspace rejection, three stop domains, and gluing witnesses;
- obstruction and gluing analysis with active incompatibilities, pairwise edges, and triple-overlap witnesses;
- design contracts and conceptual interface/record reference;
- independent financial-authorization review protocol and synthetic documentation-only record template;
- accessibility and plain-language review criteria with text-equivalent diagrams and authority-state comprehension checks;
- developer onboarding, security/privacy, operations, incident response, recovery, and ADR documentation;
- pinned documentation dependencies and strict exact-head validation workflow;
- evidence-oriented task chain, punch list, release plan, and changelog.

These are inputs to review. They do not prove that charter, contract, accessibility, authority, publication, simulation, testnet, device-trust, or production gates passed.

## Working route

```text
Authorized enrolled device
→ Repository 0 local resource proposal
→ QSO-PAYMENTS validated economic intent
→ approved review surface
→ independent financial authorization
→ Repository 1 device/workspace verification and narrow capability admission
→ disabled external adapter
→ execution evidence
→ QSO-PAYMENTS reconciliation
→ Repository 1 canonical disposition
```

This route is not operational. Device enrollment cannot create financial approval by implication. Repository `1` cannot create or broaden financial approval. QSO-PAYMENTS cannot approve or fund its own intent. A review form, interface control, trusted device, or successful workflow cannot manufacture authority. Adapter success does not establish canonical or legal finality.

## Acceptance gates

| Gate | Status | Requirement |
|---|---|---|
| Charter/payment boundary | BLOCKED | Approve purpose, users, terminology, jurisdictions, privacy/license model, subsystem role, environment model, review ownership, and prohibited capabilities. |
| Financial authority | BLOCKED | Name the independent approver and revoker; define authority source, authentication, scope, conflicts, expiry, jurisdictional assumptions, and human accountability. |
| Authorization-review protocol | DOCUMENTED / UNAPPROVED | Review exact intent/scope bindings, decision states, material-change rules, evidence classes, fail-closed stops, correction/revocation propagation, consumer acknowledgment, retention, accessibility, and prohibited inferences. |
| Portable device trust | BLOCKED | Approve device identity, enrollment generation, ownership scope, workspace/source identity, wrong-device handling, replacement, retirement, revocation, and recovery. |
| Repository `1` role | BLOCKED | Approve or replace Repository `1` as device/workspace verifier, generic capability, and canonical-disposition authority after financial approval; prohibit authority broadening. |
| Contract ownership | BLOCKED | Designate the canonical owner of device, workspace, intent, authorization, capability, receipt, dispute, reconciliation, correction, revocation, status, reason-code, and identity schemas. |
| Gluing witnesses | DOCUMENTED / UNVERIFIED | Accept the portable-trust profile, obstruction ledger, pairwise edges, triple-overlap witnesses, shared status vocabulary, and machine-readable fixture plan. |
| Contract reference | DOCUMENTED / UNAPPROVED | Review interface surfaces, envelope semantics, record families, status vocabulary, reason-code classes, examples, compatibility, and migration without treating them as an executable API. |
| Links/build/provenance | PRIOR EXACT-HEAD EVIDENCE | The updated head requires fresh immutable-source checkout, strict build, boundary scan, hashes, retained artifact, and human acceptance. |
| Claims/legal | PARTIAL | Boundaries and disclaimers exist; payment, jurisdiction, tax, finality, device-trust, autonomous-development, and economic claims require independent review. |
| Accessibility | DOCUMENTED / UNVERIFIED | Text-equivalent states, diagram prose, keyboard, focus, zoom, reflow, motion, and comprehension checks are documented; exact rendered evidence and human review remain pending. |
| Security/privacy | PARTIAL | Threats, secret prohibitions, minimization, role separation, workflow controls, incident triggers, propagation, and recovery are documented; independent review and exercises remain pending. |
| Publication/deployment | NOT AUTHORIZED | A separate decision must authorize Pages publication, verify the deployed URL and commit, and retain rollback evidence. |
| Approval | PENDING | Explicit release approval after every included-scope gate passes. |

## Required evidence package

- Approved payment-boundary charter and A.L.I.S.T.A.I.R.E. subsystem placement.
- Approved portable trust and financial-authority boundary.
- Named financial authority, authority source, revoker, conflict reviewer, capability issuer, credential/custody owner, incident owner, emergency-stop owner, recovery owner, and release owner.
- Reviewed authorization-record profile with exact intent, identity, amount, destination, environment, adapter, time, device, workspace, repository, expected-head, privacy, correction, revocation, and dispute bindings.
- Approved schema/package owner, identity namespaces, status/reason-code registries, compatibility policy, and migration plan.
- Accepted obstruction ledger and gluing-witness specification.
- Reproducible static-site bundle, source archive, source-identity record, and SHA-256 manifests tied to the immutable candidate.
- Link, rendered-accessibility, claims/legal, security/privacy, workflow-permission, and content-review reports.
- Consumer-notification, correction, revocation, withdrawal, supersession, recovery, and rollback evidence.
- Publication/provenance record and deployed-commit verification if Pages publication is approved.

## Rollback and withdrawal criteria

Withdraw or roll back if content implies production settlement, custody, guaranteed returns, autonomous transfers, device-control authority, self-authorization, legal certification, or jurisdictional approval; a complete review record is represented as financial authority; device enrollment and financial approval are ambiguous; financial approval and generic capability are conflated; environment, amount, destination, time, device, workspace, repository, adapter, or authority-source limits conflict; status meaning relies on color or diagrams; links or builds fail; sensitive data is exposed; accessibility blocks use; publication is non-reproducible; severe security/privacy findings remain; correction or revocation cannot reach every consumer; workflow provenance is incomplete; or artifact hashes differ.

Restore the previous verified source or Pages artifact, preserve rejected reports and hashes, revoke affected publication or future adapter capability, retain device and financial incident evidence, identify unreachable consumers, and preserve the recovery record.

## Unresolved blockers

- Payment charter, terminology, jurisdictional assumptions, privacy/license model, ecosystem role, reviewer ownership, and prohibited-capability boundary require approval.
- Independent financial approval, authority-source, revocation, conflict-review, and consumer-notification ownership are not designated.
- Device identity, enrollment generation, workspace/source identity, loss/theft, replacement, and revocation methods are not approved.
- Repository `1`'s exact role in capability admission and canonical disposition is not approved.
- Shared schema/package, status/reason-code, and identity-namespace ownership remain unresolved.
- Amount, precision, fee, tax, quote, replay, finality, correction, privacy, retention, device binding, and recovery semantics lack accepted machine-readable fixtures.
- Adapter credential, signing, custody, monitoring, incident, emergency-stop, and recovery topology is not approved.
- The updated exact head requires fresh strict-build and retained-artifact evidence.
- Rendered accessibility, publication, claims/legal, independent security/privacy, and exercised rollback evidence remain pending.

## Release log

- 2026-07-16 — Aligned the candidate with the documentation-only payment-boundary directive; release remained blocked by charter approval and publication evidence.
- 2026-07-19 — PR #1 established a substantial MkDocs documentation and operations package plus a release punch list; no gate was marked complete.
- 2026-07-20 — Added A.L.I.S.T.A.I.R.E. subsystem boundaries, separation of duties, capability matrix, and exact-source documentation evidence.
- 2026-07-21 — Added obstruction/gluing and portable-trust boundaries, cross-repository route constraints, identity separation, stop domains, and recovery requirements.
- 2026-07-23 — Added conceptual contract/interface and accessibility/plain-language review surfaces.
- 2026-07-23 — Added the independent financial-authorization review protocol, synthetic review-record template, exact scope and material-change rules, lifecycle states, fail-closed stops, propagation requirements, and reviewer onboarding. No financial or implementation authority was activated.
