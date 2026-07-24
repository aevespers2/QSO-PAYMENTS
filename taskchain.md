# Task Chain

States: `PROPOSED` · `READY` · `IN PROGRESS` · `BLOCKED` · `REVIEW` · `DONE`

## Product directive

- **Canonical objective:** QSO-PAYMENTS exists only as a bounded economic-intent, allocation-preview, evidence, dispute, and reconciliation subsystem of A.L.I.S.T.A.I.R.E.
- **Next objective:** Approve the documentation-only payment boundary, portable device-trust/financial-authority separation, conceptual contract reference, independent financial-authorization review protocol, and cross-repository gluing model before any executable payment simulation.
- **User outcome:** A reader can distinguish Repository `0` resource proposals and portable host observations, Repository `1` device enrollment and capability admission, QSO-PAYMENTS intents, independent financial review, attributable authorization, adapter execution, receipts, disputes, reconciliation, custody, and settlement without inferring that a complete form, trusted device, QSO, repository, interface, or technical capability can move funds.
- **MVP scope:** approved purpose, users, terminology, jurisdictional assumptions, data/privacy/license model, environment labels, subsystem ownership, financial-approval separation, device/workspace binding, loss/theft/replacement behavior, conceptual interface and record reference, independent authorization-review evidence, accessible status semantics, obstruction ledger, pairwise contracts, triple-overlap witnesses, documentation review, exact-source validation, checksums, provenance, and rollback.
- **Priority:** Charter, authority separation, portable-trust compatibility, accessible contract exposition, authorization-review evidence, and contract evidence precede schemas, accounting engines, adapters, testnet integration, or production claims.
- **Success criteria:** every economic claim is evidence-classified; device enrollment, workspace identity, proposal, validation, authorization review, authorization, capability, execution, receipt, reconciliation, and canonical disposition remain distinct; wrong-device and revoked-device use fails closed; material changes require a new review; status and authority remain understandable without color or diagrams; no credential, custody, signing, transfer, self-authorization, or guaranteed-return capability exists; accepted exact-head evidence and rollback guidance are retained.
- **Non-goals:** custody, transaction signing, autonomous transfers, self-approval, production settlement, investment products, return promises, legal/compliance certification, credentialed adapters, device surveillance, remote administration, or automatic promotion from documentation to simulation, testnet, or production.
- **Release rationale:** Financial language, device trust, and automation create elevated security, legal, privacy, accessibility, and user-expectation risk. A precise, glueable, and understandable documentation baseline is the safest useful first product.

## Working portfolio route

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

This route is a documentation candidate. Device enrollment is not financial approval. Repository `1` cannot create financial approval by itself, QSO-PAYMENTS cannot approve its own intent, and adapter success cannot force canonical acceptance. A review record remains `DOCUMENTED_NOT_AUTHORIZED` until an approved independent authority issues one exact, attributable, time-bounded decision.

## Active chain

| Priority | Task | Owner | Depends on | Status | Acceptance criteria |
|---|---|---|---|---|---|
| P0 | Approve the payment-boundary charter and portfolio role | Architect | Explicit approval | BLOCKED | Purpose, users, terminology, jurisdictions, privacy, license, environment model, prohibited claims, QSO-PAYMENTS ownership, Repository `0` proposal role, and Repository `1` candidate capability role are approved. |
| P0A | Designate financial and operational authority owners | Architect | P0 | BLOCKED | Independent financial approver/revoker, generic capability issuer/revoker, adapter credential/custody/signing owner, incident owner, emergency-stop owner, recovery owner, and release owner are named. |
| P0B | Approve portable trust and financial authority separation | Architect | P0, P0A, Repository `0`/`1` device-trust charters | REVIEW | Device enrollment, ownership scope, workspace identity, financial authorization, capability admission, wrong-device rejection, loss/theft/replacement, privacy, revocation, and recovery remain independently governed. |
| P1 | Approve obstruction and gluing model | Architect | P0, P0A, P0B | REVIEW | The active obstructions, pairwise edges, triple-overlap witnesses, result semantics, identity namespaces, schema ownership, finality limits, portable-trust bindings, and acceptance order are accepted or revised. |
| P1A | Verify documentation-only site and evidence artifact | QSOBuilder | P0, P1 | REVIEW | Exact submitted source, strict build, links, claims, accessibility, security/privacy, workflow permissions, source archive, checksums, provenance, and rollback evidence pass and are retained. |
| P1B | Review conceptual contract and accessibility references | Architect + documentation/accessibility reviewers | P0, P1 | REVIEW | Interface surfaces, record families, envelope, statuses, reason-code classes, migration requirements, diagram prose, keyboard/zoom review, and authority language are complete, consistent, and explicitly non-executable. |
| P1C | Review independent financial-authorization evidence protocol | Architect + financial/security/privacy/accessibility reviewers | P0A, P1B | REVIEW | Role separation, authority source, exact intent binding, amount/destination/environment/time/device/workspace/repository scope, conflicts, evidence classes, decision states, material-change rules, correction, revocation, dispute, consumer notification, retention, accessibility, and fail-closed stops are complete without appointing an authorizer or creating executable authority. |
| P2 | Publish machine-readable simulation-only schemas and identical fixtures | Architect | P1A, P1B, P1C, and separate approval | BLOCKED | Intent, authorization, capability, allocation, receipt, dispute, reconciliation, correction, revocation, device/workspace binding, replay, idempotency, and recovery contracts validate deterministically without credentials, custody, or transfers. |
| P3 | Implement deterministic offline simulation | Builder | P2 and separate approval | BLOCKED | Fixed-precision fictional calculations pass golden, negative, property, replay, wrong-device, partial-failure, reversal, and recovery fixtures with no external effects. |
| P4 | Evaluate isolated disabled adapter interfaces | Architect | P3 and legal/security/privacy review | BLOCKED | Adapters remain disabled by default, contain no production credentials, enforce device/workspace and authorization bindings, and cannot be represented as settlement capability. |
| P5 | Consider testnet or production work | Human authority | All prior gates and separate decision | BLOCKED | New scope, legal review, credentials, custody, monitoring, incident response, emergency stop, recovery, device enrollment, and explicit approval are independently established. |

## Documentation milestone candidate

PR #1 contains a Pages-oriented documentation package, a portfolio-level obstruction and gluing analysis, a dedicated portable trust/financial-authority boundary, a conceptual contract and interface reference, and an accessibility/plain-language review guide. The focused financial-authorization review milestone adds role separation, review states, exact bindings, a synthetic documentation-only record, fail-closed stops, correction and revocation propagation, cross-repository witnesses, and reviewer onboarding. These are candidate inputs to P0–P1C, not completion of those gates.

## Builder rules

Documentation is the only active release surface. Do not add executable transfer paths, credentials, custody, production adapter behavior, device surveillance, remote administration, or an authorization shortcut for Repository `0`, Repository `1`, QSO-PAYMENTS, QSO-STUDIO, Bridge, QSO-DIGITALIS, QSO-FABRIC, a genome, a trusted device, or a model process. Do not mark a gate complete merely because documentation builds successfully or a review record is structurally complete.

## Evidence rules

For every accepted task, retain:

- immutable source and dependency identities;
- observed facts, proposals, interpretations, recommendations, and unresolved uncertainty as separate classes;
- schema/profile versions and ownership;
- device, enrollment-generation, workspace, repository, expected-head, requester, beneficiary, approver, destination, environment, and adapter bindings where applicable;
- authority source, scope, time window, conflict-of-interest state, material-change decision, and prohibited inferences;
- positive, negative, stale, replay, wrong-identity, wrong-device, wrong-workspace, over-limit, partial-failure, revocation, correction, replacement, and recovery fixtures;
- validation commands, results, artifacts, and hashes;
- approver, issuer, verifier, revoker, incident owner, and rollback owner;
- privacy, retention, jurisdictional, claims, accessibility, keyboard, zoom, and diagram-equivalence review evidence;
- downstream correction/revocation acknowledgments, unreachable consumers, rollback instructions, and residual risks.

## Builder log

- 2026-07-19 — PR #1 substantially expanded the documentation-only candidate and added a pinned strict MkDocs build. No runtime authority or release gate was added or marked complete.
- 2026-07-20 — Defined QSO-PAYMENTS as A.L.I.S.T.A.I.R.E.'s bounded economic-intent and evidence subsystem; documented separation between autonomous-development orchestration and financial authorization; hardened exact-source documentation evidence.
- 2026-07-21 — Added the portfolio obstruction and gluing analysis, clarified the Repository `0` → QSO-PAYMENTS → financial approval → Repository `1` route, and expanded the task chain for shared contracts, fixtures, revocation, finality, and recovery. No financial or runtime authority was activated.
- 2026-07-21 — Added the portable trust and financial authority boundary, device/workspace bindings, lost-device and replacement behavior, three independent stop domains, and compatibility witnesses preventing device trust from becoming financial permission. No device-control or payment authority was activated.
- 2026-07-23 — Added the conceptual contract/interface reference and accessibility/plain-language review guide; synchronized navigation and planning controls. No schema, API, financial authority, adapter, publication, or runtime scope was activated.
- 2026-07-23 — Added the independent financial-authorization review protocol, documentation-only review-record template, material-change and conflict rules, lifecycle states, fail-closed stops, correction/revocation propagation, gluing witnesses, and reviewer onboarding. No authorizer, payment, credential, capability, adapter, publication, or runtime authority was created.
