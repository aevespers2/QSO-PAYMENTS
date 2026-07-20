# Task Chain

States: `PROPOSED` · `READY` · `IN PROGRESS` · `BLOCKED` · `REVIEW` · `DONE`

## Product directive

- **Canonical objective:** QSO-PAYMENTS exists only as a bounded economic-intent and evidence subsystem of A.L.I.S.T.A.I.R.E.
- **Next objective:** Approve and publish a documentation-only payment-intent, authorization, and A.L.I.S.T.A.I.R.E. integration boundary before any executable payment simulation.
- **User outcome:** A reader can understand how autonomous resource proposals, intent, authorization, allocation, receipts, disputes, escrow milestones, adapters, custody, and settlement differ, with clear environment and risk labels and no implication that QSOs or the autonomous-development control plane can move funds.
- **MVP scope:** approved purpose/users/terminology/jurisdictional assumptions/data/privacy/license; A.L.I.S.T.A.I.R.E. subsystem ownership and control-plane separation; documentation-only architecture; explicit simulation/testnet/production states; static-site link/HTML/accessibility/claims/security review; reproducible Pages artifact, exact-source identity, checksums, provenance, and rollback.
- **Priority:** Charter and public documentation integrity precede schemas, accounting engines, adapters, testnet integration, or production claims.
- **Success criteria:** every payment and economic claim is evidence-classified; the site deploys reproducibly; accessibility and privacy/security checks pass; no credentials, custody, signing, transfer, self-authorization, or guaranteed-return capability exists; artifact and rollback evidence are retained.
- **Non-goals:** custody, transaction signing, autonomous transfers, self-approval, production settlement, investment products, return promises, legal/compliance certification, or credentialed adapters.
- **Release rationale:** Payment language creates elevated legal, security, and user-expectation risk. A precise documentation baseline is the safest useful first product and the prerequisite for a later simulation-only contract set.

## Active chain

| Priority | Task | Owner | Depends on | Status | Acceptance criteria |
|---|---|---|---|---|---|
| P0 | Approve the payment-boundary charter and A.L.I.S.T.A.I.R.E. subsystem role | Architect | User approval | BLOCKED | Purpose, users, terminology, jurisdictions, ecosystem role, autonomous-development control-plane separation, financial authority ownership, data/privacy model, license, environment labels, and prohibited capabilities are approved. |
| P1 | Verify the documentation-only site and publication artifact | QSOBuilder | P0 | REVIEW | Exact submitted source, strict build, links, HTML/CSS, claims, accessibility, security/privacy, workflow permissions, reproducible artifact, checksums, provenance, deployment, and rollback evidence pass. |
| P2 | Publish versioned simulation-only schemas and fixtures | Architect | P1 and separate approval | BLOCKED | Intent, authorization, allocation, receipt, dispute, reconciliation, rounding, replay, and idempotency contracts validate deterministically without credentials, custody, or transfers. |
| P3 | Evaluate disabled adapter interfaces | Architect | P2 and legal/security review | BLOCKED | Adapters remain disabled by default, contain no production credentials, and cannot be represented as settlement capability. |

## Documentation milestone candidate

PR #1 now contains a complete Pages-oriented documentation package: project and portfolio boundary, authority architecture, proposed contract semantics, trust and privacy model, onboarding, incident response, rollback, ADR-0001, strict MkDocs configuration, A.L.I.S.T.A.I.R.E. integration and capability matrix, and an exact-source build that retains a SHA-256 evidence artifact. This is candidate input to P0/P1, not completion of either gate. Charter approval, accessibility and claims review, accepted security/privacy review, deployment verification, and exercised rollback evidence remain required.

## Builder rules

Documentation is the only active release surface. Do not add executable transfer paths, credentials, custody, production adapter behavior, or an authorization shortcut for the autonomous-development control plane. Do not mark P0 or P1 complete merely because documentation builds successfully.

## Builder log

- 2026-07-19 — PR #1 substantially expanded the documentation-only candidate and added a pinned strict MkDocs build. No runtime authority or release gate was added or marked complete.
- 2026-07-20 — Defined QSO-PAYMENTS as A.L.I.S.T.A.I.R.E.'s bounded economic-intent and evidence subsystem; documented the separation between autonomous-development orchestration and financial authorization; hardened the Pages build to verify the submitted head and retain source/hash evidence.
- Record future approvals, commits, publication runs, claim/accessibility/security reports, schema and fixture hashes if later authorized, artifact checksums, rollback evidence, and follow-ups.
