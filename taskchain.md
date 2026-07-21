# Task Chain

States: `PROPOSED` · `READY` · `IN PROGRESS` · `BLOCKED` · `REVIEW` · `DONE`

## Product directive

- **Canonical objective:** QSO-PAYMENTS exists only as a bounded economic-intent, allocation-preview, evidence, dispute, and reconciliation subsystem of A.L.I.S.T.A.I.R.E.
- **Next objective:** Approve the documentation-only payment boundary and the cross-repository gluing model before any executable payment simulation.
- **User outcome:** A reader can distinguish Repository `0` resource proposals, QSO-PAYMENTS intents, independent financial approval, Repository `1` capability admission, adapter execution, receipts, disputes, reconciliation, custody, and settlement without inferring that a QSO or repository can move funds.
- **MVP scope:** approved purpose, users, terminology, jurisdictional assumptions, data/privacy/license model, environment labels, subsystem ownership, financial-approval separation, obstruction ledger, pairwise contracts, triple-overlap witnesses, documentation review, exact-source validation, checksums, provenance, and rollback.
- **Priority:** Charter, authority separation, and contract compatibility precede schemas, accounting engines, adapters, testnet integration, or production claims.
- **Success criteria:** every economic claim is evidence-classified; proposal, authorization, capability, execution, receipt, reconciliation, and canonical disposition remain distinct; no credential, custody, signing, transfer, self-authorization, or guaranteed-return capability exists; accepted exact-head evidence and rollback guidance are retained.
- **Non-goals:** custody, transaction signing, autonomous transfers, self-approval, production settlement, investment products, return promises, legal/compliance certification, credentialed adapters, or automatic promotion from documentation to simulation, testnet, or production.
- **Release rationale:** Financial language and automation create elevated security, legal, privacy, and user-expectation risk. A precise, glueable documentation baseline is the safest useful first product.

## Working portfolio route

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

This route is a documentation candidate. Repository `1` cannot create financial approval by itself, QSO-PAYMENTS cannot approve its own intent, and adapter success cannot force canonical acceptance.

## Active chain

| Priority | Task | Owner | Depends on | Status | Acceptance criteria |
|---|---|---|---|---|---|
| P0 | Approve the payment-boundary charter and portfolio role | Architect | Explicit approval | BLOCKED | Purpose, users, terminology, jurisdictions, privacy, license, environment model, prohibited claims, QSO-PAYMENTS ownership, Repository `0` proposal role, and Repository `1` candidate capability role are approved. |
| P0A | Designate financial and operational authority owners | Architect | P0 | BLOCKED | Independent financial approver/revoker, generic capability issuer/revoker, adapter credential/custody/signing owner, incident owner, emergency-stop owner, recovery owner, and release owner are named. |
| P1 | Approve obstruction and gluing model | Architect | P0, P0A | REVIEW | The 18 active obstructions, pairwise edges, triple-overlap witnesses, result semantics, identity namespaces, schema ownership, finality limits, and acceptance order are accepted or revised. |
| P1A | Verify documentation-only site and evidence artifact | QSOBuilder | P0, P1 | REVIEW | Exact submitted source, strict build, links, claims, accessibility, security/privacy, workflow permissions, source archive, checksums, provenance, and rollback evidence pass and are retained. |
| P2 | Publish machine-readable simulation-only schemas and identical fixtures | Architect | P1A and separate approval | BLOCKED | Intent, authorization, capability, allocation, receipt, dispute, reconciliation, correction, revocation, replay, idempotency, and recovery contracts validate deterministically without credentials, custody, or transfers. |
| P3 | Implement deterministic offline simulation | Builder | P2 and separate approval | BLOCKED | Fixed-precision fictional calculations pass golden, negative, property, replay, partial-failure, reversal, and recovery fixtures with no external effects. |
| P4 | Evaluate isolated disabled adapter interfaces | Architect | P3 and legal/security/privacy review | BLOCKED | Adapters remain disabled by default, contain no production credentials, and cannot be represented as settlement capability. |
| P5 | Consider testnet or production work | Human authority | All prior gates and separate decision | BLOCKED | New scope, legal review, credentials, custody, monitoring, incident response, emergency stop, recovery, and explicit approval are independently established. |

## Documentation milestone candidate

PR #1 now contains a Pages-oriented documentation package and a portfolio-level obstruction and gluing analysis. The new analysis separates financial approval from generic capability issuance, identifies 18 compatibility obstructions, defines eight pairwise contract edges and six triple-overlap witnesses, and records explicit non-finality and recovery semantics. This is candidate input to P0–P1A, not completion of those gates.

## Builder rules

Documentation is the only active release surface. Do not add executable transfer paths, credentials, custody, production adapter behavior, or an authorization shortcut for Repository `0`, Repository `1`, QSO-PAYMENTS, QSO-STUDIO, Bridge, QSO-DIGITALIS, QSO-FABRIC, a genome, or a model process. Do not mark a gate complete merely because documentation builds successfully.

## Evidence rules

For every accepted task, retain:

- immutable source and dependency identities;
- observed facts, proposals, and unresolved uncertainty;
- schema/profile versions and ownership;
- positive, negative, stale, replay, wrong-identity, over-limit, partial-failure, revocation, correction, and recovery fixtures where applicable;
- validation commands, results, artifacts, and hashes;
- approver, issuer, verifier, revoker, incident owner, and rollback owner;
- privacy, retention, jurisdictional, claims, and accessibility review evidence;
- rollback instructions and residual risks.

## Builder log

- 2026-07-19 — PR #1 substantially expanded the documentation-only candidate and added a pinned strict MkDocs build. No runtime authority or release gate was added or marked complete.
- 2026-07-20 — Defined QSO-PAYMENTS as A.L.I.S.T.A.I.R.E.'s bounded economic-intent and evidence subsystem; documented separation between autonomous-development orchestration and financial authorization; hardened exact-source documentation evidence.
- 2026-07-21 — Added the portfolio obstruction and gluing analysis, clarified the Repository `0` → QSO-PAYMENTS → financial approval → Repository `1` route, and expanded the task chain for shared contracts, fixtures, revocation, finality, and recovery. No financial or runtime authority was activated.
