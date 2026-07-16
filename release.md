# Release Plan

## Current Decision
Status: `BLOCKED — PAYMENT CHARTER AND PUBLICATION EVIDENCE REQUIRED`

QSO-PAYMENTS is no longer empty. Reviewed documentation head `565f8bb4e7873fb26ce73aec81548e8517768272` contains a README, a styled GitHub Pages site, and a Pages deployment workflow describing an intent/authorization/settlement separation and denying autonomous custody or production-transfer authority. No release is eligible because `taskchain.md` and `punchlist.md` are absent, the payment charter and jurisdictional/compliance assumptions are unapproved, no current deployment/build/link/accessibility/security/privacy result is attached, and there are no versioned schemas, deterministic fixtures, accounting tests, provenance, checksums, or rollback artifact.

## Versioning
- Use Semantic Versioning only after the documentation identity, payment charter, jurisdictional assumptions, license, publication target, and simulation-vs-production boundary are approved.
- First possible documentation candidate: `0.0.1-docs.1`.
- First executable candidate must be simulation-only and remain pre-release until contract, accounting, security, and provenance gates pass.
- No version or page may imply production custody, settlement, investment returns, or autonomous transfer capability.

## Candidate Scope
### Documentation-only candidate
- Approved purpose, users, non-goals, terminology, jurisdictions, data classification, privacy model, license, and ecosystem relationships.
- Explicit separation of intent, authorization, allocation, receipt, dispute, escrow milestone, custody, adapter execution, and settlement.
- Clear simulation, testnet, and production states with disabled-by-default adapters.
- Reproducible static-site publication with link, HTML, accessibility, security/privacy, and claims review.
- Publication artifact, checksums, provenance, and rollback instructions.

### Later simulation candidate
- Versioned declarative payment-intent, authorization, allocation, receipt, dispute, and reconciliation schemas.
- Deterministic fixtures for splits, royalties, validator rewards, pooled treasury, escrow milestones, failed authorization, disputes, rounding, replay, idempotency, and reconciliation.
- No credentials, custody, direct transfer authority, autonomous execution, or production settlement.

## Existing Candidate Assets
- `README.md` defines an audit-oriented payment-contract purpose and states that QSOs do not custody assets, sign transactions, or execute production transfers.
- `docs/index.html` presents the intent/policy/adapter architecture, distribution routes, explicit environments, freeze behavior, and a non-financial-product disclaimer.
- `docs/styles.css` provides the current presentation layer.
- `.github/workflows/pages.yml` deploys `docs/` with `contents: read`, `pages: write`, `id-token: write`, disabled checkout credentials, concurrency control, and a ten-minute timeout.

These are documentation and deployment inputs, not releasable completed work until their claims, workflow result, accessibility, security/privacy, provenance, and approval are verified at one immutable commit.

## Selected Completed Work
None selected for release. The site and workflow exist, but no approved task, completed punch-list item, retained publication result, claim audit, accessibility/security review, checksummed artifact, or provenance manifest establishes a releasable documentation snapshot.

## Planned Changelog Entries
- `Documentation`: approved payment charter, terminology, environment model, non-goals, compliance assumptions, ecosystem role, and adapter boundary.
- `Changed`: evidence-classified capability wording and explicit separation of documentation, simulation, testnet, and production states.
- `Security`: authorization, custody, credential, privacy, replay/idempotency, ledger, dependency, workflow-permission, and supply-chain findings.
- `Accessibility`: navigation, semantics, keyboard path, contrast, scaling, and error/notice presentation evidence.
- `Added`: simulation-only schemas, fixtures, validators, and reconciliation reports only after implementation gates pass.
- `Release`: reproducible site/source artifacts, reports, checksums, provenance, and approval decision.

## Acceptance Gates
| Gate | Status | Requirement |
|---|---|---|
| Charter/payment boundary | BLOCKED | Approve purpose, users, terminology, jurisdictions, license, ecosystem role, simulation-only implementation boundary, and prohibited production capabilities. |
| Task completion | FAIL | Create `taskchain.md` and `punchlist.md`; complete the included documentation or simulation task with linked evidence. |
| Publication/deployment | NO CURRENT EVIDENCE | Pages workflow succeeds at the immutable candidate commit and the published URL/artifact is retained in evidence. |
| Link/HTML/build validation | NO EVIDENCE | Internal/external links, HTML, CSS references, metadata, responsive layout, and reproducible static bundle pass. |
| Claims/compliance review | PARTIAL | Safety disclaimers exist; every payment, route, authorization, adapter, environment, and economic claim must be evidence-classified and reviewed. |
| Accessibility | NO EVIDENCE | Semantic structure, keyboard navigation, focus, contrast, scaling, reduced motion where applicable, and notice readability pass. |
| Security/privacy | NO EVIDENCE | No credentials/custody/transfers; dependency, secret, workflow, external-link, content, privacy, and supply-chain checks pass. |
| Contract/accounting validation | NOT IN DOCS CANDIDATE | Required only for an executable candidate: schemas, fixtures, allocation, rounding, idempotency, replay, disputes, and reconciliation pass deterministically. |
| Documentation | PARTIAL | README and landing page exist; approved charter, exact publication commands, limitations, compliance assumptions, operations, and rollback remain incomplete. |
| Provenance | NO EVIDENCE | Candidate commit, workflow run, tool/action versions, commands, publication artifact, hashes, repository URL, and attestations are recorded. |
| Approval | PENDING | Explicit release approval after all included-scope gates pass. |

## Artifact Requirements
- Approved payment-boundary charter, threat/compliance model, and capability-claim inventory.
- Reproducible static-site bundle and source archive for a documentation candidate.
- Link, HTML, accessibility, claims, security/privacy, and workflow-permission reports.
- For a later simulation candidate: versioned schemas, deterministic positive/negative fixtures, accounting/reconciliation reports, tests, and SBOM where applicable.
- SHA-256 checksum manifest, publication/provenance record, and rollback artifact tied to the candidate commit.

## Rollback Criteria
Withdraw or roll back if published content implies production settlement, custody, guaranteed returns, or autonomous transfers; authorization/accounting semantics are ambiguous; environment labels are misleading; links or deployment fail; personal or confidential data is exposed; accessibility blocks use; severe security/compliance findings remain; publication cannot be reproduced; or artifact hashes differ. Restore the previous verified Pages artifact/tag and preserve failed-candidate reports and hashes.

## Unresolved Blockers
- Approval is required for the payment charter, simulation/production boundary, terminology, jurisdictional assumptions, license, privacy/data model, and ecosystem role.
- `taskchain.md` and `punchlist.md` do not exist, so the current documentation has no formal completion evidence.
- No current Pages deployment result, site artifact, link/HTML check, accessibility report, claim/compliance audit, security/privacy report, checksum, or provenance manifest is attached to the reviewed documentation head.
- The site describes settlement adapters and economic routes, but no executable schemas, validators, fixtures, accounting tests, or adapter controls exist; these remain documentation-only claims.
- No release rollback artifact or verified prior publication baseline is recorded.

## Release Log
- 2026-07-16: Corrected the prior empty-repository assessment after identifying the Pages site and deployment workflow; candidate remains `BLOCKED — PAYMENT CHARTER AND PUBLICATION EVIDENCE REQUIRED`.
