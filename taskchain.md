# Task Chain

States: `PROPOSED` · `READY` · `IN PROGRESS` · `BLOCKED` · `REVIEW` · `DONE`

## Product directive

- **Next objective:** Approve and publish a documentation-only payment-intent and authorization boundary before any executable payment simulation.
- **User outcome:** A reader can understand how intent, authorization, allocation, receipts, disputes, escrow milestones, adapters, custody, and settlement differ, with clear environment and risk labels and no implication that QSOs can move funds.
- **MVP scope:** approved purpose/users/terminology/jurisdictional assumptions/data/privacy/license; documentation-only architecture; explicit simulation/testnet/production states; static-site link/HTML/accessibility/claims/security review; reproducible Pages artifact, checksums, provenance, and rollback.
- **Priority:** Charter and public documentation integrity precede schemas, accounting engines, adapters, testnet integration, or production claims.
- **Success criteria:** every payment and economic claim is evidence-classified; the site deploys reproducibly; accessibility and privacy/security checks pass; no credentials, custody, signing, transfer, or guaranteed-return capability exists; artifact and rollback evidence are retained.
- **Non-goals:** custody, transaction signing, autonomous transfers, production settlement, investment products, return promises, legal/compliance certification, or credentialed adapters.
- **Release rationale:** Payment language creates elevated legal, security, and user-expectation risk. A precise documentation baseline is the safest useful first product and the prerequisite for a later simulation-only contract set.

## Active chain

| Priority | Task | Owner | Depends on | Status | Acceptance criteria |
|---|---|---|---|---|---|
| P0 | Approve the payment-boundary charter | Architect | User approval | BLOCKED | Purpose, users, terminology, jurisdictions, ecosystem role, data/privacy model, license, environment labels, and prohibited capabilities are approved. |
| P1 | Verify the documentation-only site and publication artifact | QSOBuilder | P0 | PROPOSED | Links, HTML/CSS, claims, accessibility, security/privacy, workflow permissions, reproducible Pages artifact, checksums, provenance, and rollback pass. |
| P2 | Publish versioned simulation-only schemas and fixtures | Architect | P1 and separate approval | BLOCKED | Intent, authorization, allocation, receipt, dispute, reconciliation, rounding, replay, and idempotency contracts validate deterministically without credentials, custody, or transfers. |
| P3 | Evaluate disabled adapter interfaces | Architect | P2 and legal/security review | BLOCKED | Adapters remain disabled by default, contain no production credentials, and cannot be represented as settlement capability. |

## Documentation milestone candidate

PR #1 now contains a complete Pages-oriented documentation package: project and portfolio boundary, authority architecture, proposed contract semantics, trust and privacy model, onboarding, incident response, rollback, ADR-0001, strict MkDocs configuration, and pull-request build verification. This is candidate input to P1, not completion of P0 or P1. Charter approval, exact-head validation evidence, accessibility and claims review, artifact hashes, provenance, deployment verification, and rollback evidence remain required.

## Builder rules

Documentation is the only active release surface. Do not add executable transfer paths, credentials, custody, or production adapter behavior. Do not mark P0 or P1 complete merely because documentation builds successfully.

## Builder log

- 2026-07-19 — PR #1 substantially expanded the documentation-only candidate and added a pinned strict MkDocs build. No runtime authority or release gate was added or marked complete.
- Record future approvals, commits, publication runs, claim/accessibility/security reports, schema and fixture hashes if later authorized, artifact checksums, rollback evidence, and follow-ups.
