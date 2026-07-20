# QSO-PAYMENTS

Auditable payment-intent, authorization, allocation, receipt, dispute, reconciliation, and disabled settlement-adapter boundaries for the A.L.I.S.T.A.I.R.E. and Quantum State Object ecosystem.

> **Current release surface: documentation only.** QSO-PAYMENTS does not custody assets, sign transactions, hold credentials, execute testnet or production transfers, provide investment products, or promise returns.

## A.L.I.S.T.A.I.R.E. role

A.L.I.S.T.A.I.R.E. is the canonical system objective. QSO-PAYMENTS is its bounded **economic-intent and evidence subsystem**: it may document resource needs, proposed budgets, approval requests, allocations, receipts, disputes, and reconciliation states. It is not the autonomous-development control plane and does not grant that control plane financial authority.

Autonomous workflows may prepare and verify a resource request. They may not approve their own request, inherit credentials, sign transactions, custody assets, or infer settlement from incomplete evidence. See [A.L.I.S.T.A.I.R.E. integration](docs/ALISTAIRE_INTEGRATION.md).

## Documentation

- [GitHub Pages source](docs/index.md)
- [Project guide](docs/PROJECT_GUIDE.md)
- [Architecture and trust boundaries](docs/ARCHITECTURE.md)
- [A.L.I.S.T.A.I.R.E. integration](docs/ALISTAIRE_INTEGRATION.md)
- [Design contracts](docs/DESIGN_CONTRACTS.md)
- [Developer onboarding](docs/ONBOARDING.md)
- [Security and privacy](docs/SECURITY_PRIVACY.md)
- [Operations and recovery](docs/OPERATIONS.md)
- [Architecture decisions](docs/decisions/0001-documentation-only-boundary.md)
- [Task chain](taskchain.md)
- [Release plan](release.md)
- [Changelog](changelog.md)

## Product boundary

```text
A.L.I.S.T.A.I.R.E. objective or bounded human/QSO proposal
-> payment intent
-> schema and policy validation
-> independent authorization
-> deterministic allocation and reconciliation
-> disabled external-adapter boundary
-> receipt, failure, unknown, or dispute evidence
```

A proposal is not authorization. Authorization is not settlement. A receipt is adapter-reported evidence, not an unconditional claim of finality. Documentation and simulation evidence do not establish production capability.

## Environment model

- **Documentation — current:** concepts, contracts, risks, review procedures, and publication evidence.
- **Simulation — future approval:** deterministic fictional calculations with no credentials, custody, signing, or external transfers.
- **Testnet — not authorized:** separately governed non-production integration.
- **Production — prohibited by current scope:** independently authorized, audited, monitored, and legally reviewed deployment.

Only the documentation environment is currently in release scope.

## Build the documentation

```bash
python -m venv .venv
. .venv/bin/activate
python -m pip install -r requirements-docs.txt
mkdocs build --strict
```

The Pages workflow builds the pinned MkDocs site on documentation pull requests and deploys the generated `site/` artifact only from `main`. Pull-request builds assert the submitted head commit, generate a SHA-256 manifest, and retain a review artifact. A successful build is verification input, not release approval; the exact workflow run, artifact, checksums, accessibility review, claims review, security/privacy review, provenance, and rollback record must be retained for one immutable candidate commit.

## Safety boundary

- QSOs and autonomous-development workflows may produce bounded, reviewable payment intents; they cannot approve their own intents.
- External adapters remain disabled until separately authorized, tested, audited, and operationally governed.
- Credentials, private keys, and sensitive account identifiers must not appear in repository records, fixtures, logs, or public artifacts.
- Allocation totals must reconcile under explicit fixed-precision, rounding, and remainder rules or fail closed.
- Retries require idempotency and cannot duplicate a previously accepted route.
- Missing or contradictory evidence remains unresolved instead of being represented as successful settlement.
- No documentation page constitutes a financial product, custody service, settlement service, legal certification, or promise of returns.
