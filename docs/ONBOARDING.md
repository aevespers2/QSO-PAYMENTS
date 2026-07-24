# Developer onboarding

QSO-PAYMENTS is currently a documentation-only repository. Contributor work must improve clarity, evidence, reviewability, or publication quality without creating executable payment behavior or implying authorization that has not been granted.

## Prerequisites

- Git
- Python 3.11 or newer
- A clean virtual environment
- No payment credentials, private keys, account identifiers, production records, or private financial communications

## Local documentation setup

```bash
git clone https://github.com/aevespers2/QSO-PAYMENTS.git
cd QSO-PAYMENTS
python -m venv .venv
. .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements-docs.txt
mkdocs serve
```

On Windows PowerShell, activate with `.venv\Scripts\Activate.ps1`.

Build the exact publication candidate before opening a pull request:

```bash
mkdocs build --strict
```

The generated `site/` directory is disposable build output and must not be treated as release evidence unless it is produced from an immutable commit by the approved workflow and its checksum and provenance are retained.

## Required reading order

1. `README.md`
2. `taskchain.md`
3. `release.md`
4. `changelog.md`
5. `docs/PROJECT_GUIDE.md`
6. `docs/ARCHITECTURE.md`
7. `docs/ALISTAIRE_INTEGRATION.md`
8. `docs/PORTABLE_TRUST_FINANCIAL_BOUNDARY.md`
9. `docs/CONTRACT_REFERENCE.md`
10. `docs/FINANCIAL_AUTHORIZATION_REVIEW.md`
11. `docs/ACCESSIBILITY_REVIEW.md`
12. `docs/SECURITY_PRIVACY.md`
13. `docs/OPERATIONS.md`

Read the authorization-review guide before editing any page that uses approval, permission, capability, execution, receipt, settlement, finality, revocation, or recovery language.

## Scope discipline

Documentation changes may:

- define terms and responsibilities;
- clarify authority and trust boundaries;
- describe proposed records, review protocols, and invariants;
- add diagrams, examples, threat analysis, onboarding, or review procedures;
- improve navigation, accessibility, reproducibility, provenance, and rollback readiness;
- correct claims that overstate current capability.

Documentation changes must not:

- appoint an independent financial authority or imply that one has been appointed;
- add executable transfer, signing, custody, or adapter behavior;
- include real credentials, private keys, account numbers, payment addresses, private device identifiers, production records, or personal financial data;
- represent a complete form, successful workflow, trusted device, simulation, or testnet behavior as financial approval or production readiness;
- promise returns, legal compliance, finality, reversibility, or suitability;
- mark an authority or release gate complete without retained evidence and the responsible human decision;
- invent charter approval, jurisdictional conclusions, consumer acknowledgment, or publication authority.

## Writing conventions

Use the following words precisely:

- **proposal** for an economic request that has no authority;
- **intent** for a structured proposal record;
- **validation** for schema and policy evaluation without approval;
- **review** for evidence inspection that may remain blocked or indeterminate;
- **authorization** for one exact, independent, attributable, time-bounded, revocable approval under an approved authority source;
- **capability** for a narrower technical permission that cannot create or broaden financial authorization;
- **allocation** for deterministic decomposition of an approved total;
- **submission** for a separately authorized adapter handoff;
- **receipt** or **adapter evidence** for what a named adapter reported;
- **reconciliation** for comparison of expected and reported outcomes;
- **dispute** for a preserved challenge to evidence or interpretation;
- **correction** for a linked record that repairs a defect without deleting history;
- **revocation** for an attributable prohibition on future use;
- **settlement** and **finality** only when their exact external-system and legal assumptions are stated.

Every capability and decision statement should identify its environment: documentation, simulation, testnet, or production. Every authorization statement should identify the exact intent, authority source, scope, time window, and prohibited effects.

## Example and fixture rules

All examples must be fictional, deterministic, and clearly labeled. Use neutral identifiers such as `subject-001`, `route-alpha`, and `SIM-UNIT`; avoid realistic account numbers, wallet addresses, personal names, private communications, or data copied from external systems.

Examples should include negative and unresolved cases: missing authorizer, ambiguous authority source, conflict of interest, stale evidence, wrong identity, wrong destination, wrong device/workspace/head, over-limit scope, expiry, duplicate detection, arithmetic failure, revocation, correction, dispute, partial result, unreachable consumer, and failed recovery.

An invalid placeholder digest must be described as invalid so it cannot be mistaken for an accepted fixture.

## Pull-request checklist

- [ ] The change is documentation-only.
- [ ] README, Pages, task chain, punch list, release plan, and changelog remain consistent.
- [ ] No authority, approval, certification, publication, or release gate is implied without evidence.
- [ ] Environment labels and current maturity are explicit.
- [ ] Proposal, validation, review, authorization, capability, allocation, adapter action, evidence, reconciliation, dispute, custody, settlement, and finality remain separate.
- [ ] Material changes require a new review rather than silent broadening.
- [ ] Correction, revocation, withdrawal, supersession, consumer notification, recovery, and rollback effects are described when relevant.
- [ ] Observed facts, interpretations, recommendations, missing evidence, disputes, and privacy restrictions remain distinct.
- [ ] No secrets or sensitive personal, device, network, or financial metadata are present.
- [ ] Claims avoid custody, settlement, investment, certification, jurisdictional approval, or guaranteed-return implications.
- [ ] Links, headings, tables, code blocks, diagrams, and prose alternatives are valid.
- [ ] `mkdocs build --strict` passes from a clean environment.
- [ ] Accessibility, provenance, retention, and rollback effects are described when relevant.

## Review roles

A documentation reviewer checks clarity, consistency, navigation, links, accessibility, examples, and evidence classification. An architecture reviewer checks authority boundaries, invariants, lifecycle, terminology, gluing, migration, and repository relationships. A financial-authority reviewer checks authority source, exact scope, conflicts, expiry, revocation, prohibited effects, and human accountability without also serving as the proposer or capability issuer unless an approved exception is independently reviewed.

Security, privacy, legal, accessibility, incident, recovery, and release reviewers remain independent gates where their approval is required. Documentation review and workflow success do not substitute for any of them.
