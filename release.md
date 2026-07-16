# Release Plan

## Current Decision
Status: `BLOCKED — PAYMENT BOUNDARY APPROVAL REQUIRED`

QSO-PAYMENTS is empty. It has no `taskchain.md`, `punchlist.md`, charter, schemas, implementation, tests, workflows, security/compliance evidence, documentation, provenance, artifacts, or rollback baseline. No release is eligible, and no production payment, custody, settlement, investment-return, or autonomous-transfer capability may be implied.

## Versioning
- Use Semantic Versioning only after the repository charter, jurisdictional/compliance assumptions, and simulation-vs-production boundary are approved.
- First possible documentation-only candidate: `0.0.1-charter.1`.
- First implementation candidate must be simulation-only unless a separately approved, independently reviewed settlement adapter is later authorized.

## Candidate Scope
### Charter candidate
- Purpose, users, non-goals, data classification, trust boundary, jurisdictions, licensing, and relationship to QuantumStateObjects/QSO-GENOMES/QSO-FABRIC.
- Explicit separation of intent, authorization, allocation, receipt, dispute, escrow milestone, custody, and settlement.
- Simulation, testnet, and production states must be unambiguous.

### Later simulation candidate
- Versioned declarative payment-intent and allocation schemas.
- Deterministic fixtures for splits, royalties, validator rewards, pooled treasury, escrow milestones, failed authorization, disputes, and reconciliation.
- No credentials, custody, direct transfer authority, autonomous execution, or production settlement.

## Selected Completed Work
None. The repository contains no releaseable content.

## Planned Changelog Entries
- `Documentation`: approved payment-boundary charter, terminology, non-goals, and compliance assumptions.
- `Added`: simulation-only schemas, fixtures, validator, and reconciliation reports after approval.
- `Security`: authorization, custody, credential, replay/idempotency, ledger, dependency, workflow, and supply-chain findings.
- `Release`: deterministic reports, checksums, provenance, and approval decision.

## Acceptance Gates
| Gate | Status | Requirement |
|---|---|---|
| Charter/payment boundary | BLOCKED | Approve simulation-only scope, terminology, jurisdictions, license, ecosystem role, and prohibited production capabilities. |
| Task completion | FAIL | Task chain and punch list exist; included work is `DONE` with evidence. |
| Contract validation | NO EVIDENCE | Versioned schemas and positive/negative fixtures validate deterministically. |
| Tests/accounting | NO EVIDENCE | Allocation, rounding, idempotency, replay, disputes, reconciliation, and failed-authorization tests pass. |
| Security/compliance | NO EVIDENCE | No credentials/custody/transfers; dependency, secret, authorization, ledger, privacy, workflow, and supply-chain checks pass. |
| Documentation | FAIL | Setup, terminology, limitations, risk, compliance assumptions, and rollback are absent. |
| Provenance | NO EVIDENCE | Commit, tools, commands, fixture/report hashes, SBOM where applicable, and attestations recorded. |
| Approval | PENDING | Explicit release approval after all blocking gates pass. |

## Artifact Requirements
- Approved charter and threat/compliance model.
- Versioned simulation schemas and deterministic positive/negative fixtures.
- Accounting, reconciliation, security, privacy, and documentation reports.
- Source/package artifacts, SBOM where applicable, SHA-256 checksums, and provenance manifest.

## Rollback Criteria
Withdraw a candidate if scope implies production settlement, custody, guaranteed returns, or autonomous transfers; if authorization or accounting semantics are ambiguous; if replay/idempotency fails; if records are non-reproducible; if severe security/compliance findings remain; or if artifact hashes differ. Restore the previous verified tag and preserve failed-candidate evidence.

## Unresolved Blockers
- Approval is required for the payment charter, simulation boundary, terminology, jurisdictional assumptions, license, and ecosystem role.
- Repository is empty; `taskchain.md` and `punchlist.md` do not exist.
- No schemas, fixtures, implementation, tests, CI, security/compliance review, documentation, provenance, or artifacts exist.

## Release Log
- 2026-07-16: Empty payment repository evaluated and held `BLOCKED — PAYMENT BOUNDARY APPROVAL REQUIRED`.