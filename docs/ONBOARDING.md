# Developer onboarding

QSO-PAYMENTS is currently a documentation-only repository. Contributor work must improve clarity, evidence, reviewability, or publication quality without creating executable payment behavior or implying authorization that has not been granted.

## Prerequisites

- Git
- Python 3.11 or newer
- A clean virtual environment
- No payment credentials, private keys, account identifiers, or production data

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
7. `docs/DESIGN_CONTRACTS.md`
8. `docs/SECURITY_PRIVACY.md`
9. `docs/OPERATIONS.md`

## Scope discipline

Documentation changes may:

- define terms and responsibilities;
- clarify authority and trust boundaries;
- describe proposed records and invariants;
- add diagrams, examples, threat analysis, or review procedures;
- improve navigation, accessibility, and reproducibility;
- correct claims that overstate current capability.

Documentation changes must not:

- add executable transfer, signing, custody, or adapter behavior;
- include real credentials, private keys, account numbers, payment addresses, or personal financial data;
- represent simulation or testnet behavior as production readiness;
- promise returns, legal compliance, finality, reversibility, or suitability;
- mark a release gate complete without retained evidence;
- invent charter approval, jurisdictional conclusions, or publication authority.

## Writing conventions

Use the following words precisely:

- **proposal** for an economic request that has no authority;
- **intent** for a structured proposal record;
- **validation** for schema and policy evaluation;
- **authorization** for an independent, attributable approval;
- **allocation** for deterministic decomposition of an approved total;
- **submission** for a separately authorized adapter handoff;
- **receipt** for adapter-reported evidence;
- **reconciliation** for comparison of expected and reported outcomes;
- **dispute** for a preserved challenge to evidence or interpretation.

Every capability statement should identify its environment: documentation, simulation, testnet, or production.

## Example and fixture rules

All examples must be fictional, deterministic, and clearly labeled. Use neutral identifiers such as `subject-001`, `route-alpha`, and `SIM-UNIT`; avoid realistic account numbers, wallet addresses, personal names, or data copied from external systems. Examples should include negative cases, unresolved states, expiry, duplicate detection, arithmetic failure, revocation, and partial-result handling.

## Pull-request checklist

- [ ] The change is documentation-only.
- [ ] The task chain, release plan, and changelog remain consistent.
- [ ] No approval or release gate is implied without evidence.
- [ ] Environment labels are explicit.
- [ ] Intent, authorization, allocation, adapter, receipt, reconciliation, and dispute remain separate.
- [ ] No secrets or sensitive financial metadata are present.
- [ ] Claims avoid custody, settlement, investment, certification, or guaranteed-return implications.
- [ ] Links and headings are valid.
- [ ] `mkdocs build --strict` passes from a clean environment.
- [ ] Accessibility and rollback effects are described when relevant.

## Review roles

A documentation reviewer checks clarity, consistency, navigation, links, accessibility, and evidence classification. An architecture reviewer checks authority boundaries, invariants, lifecycle, terminology, and repository relationships. Security, privacy, legal, and release reviewers remain independent gates where their approval is required; documentation review does not substitute for them.
