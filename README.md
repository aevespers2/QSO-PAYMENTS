# QSO-PAYMENTS

Auditable payment-intent, authorization, allocation, receipt, dispute, and settlement-adapter boundaries for the QSO ecosystem.

> **Current release surface:** documentation only. QSO-PAYMENTS does not custody assets, sign transactions, hold credentials, or execute production transfers.

## Documentation

- [Public project page](docs/index.html)
- [Project guide and onboarding](docs/PROJECT_GUIDE.md)
- [Architecture and trust boundaries](docs/ARCHITECTURE.md)
- [Task chain](taskchain.md)
- [Release plan](release.md)
- [Changelog](changelog.md)

## Product boundary

```text
QSO or human proposal
-> payment intent
-> schema and policy validation
-> independent authorization
-> allocation and reconciliation
-> disabled external-adapter boundary
-> receipt, failure, or dispute evidence
```

A proposal is not authorization. Authorization is not settlement. Documentation and simulation evidence do not establish production capability.

## Environment model

- **Documentation:** concepts, contracts, risks, and review procedures.
- **Simulation:** deterministic fictional calculations with no credentials or external transfers.
- **Testnet:** separately approved non-production integration.
- **Production:** independently authorized, audited, monitored, and legally reviewed deployment.

Only the documentation environment is currently in release scope.

## GitHub Pages

The project site is published from the `docs/` directory through the Pages workflow in `.github/workflows/pages.yml`. Publication is not considered release evidence until the exact workflow run, artifact, checksums, accessibility review, claims review, security/privacy review, provenance, and rollback record are retained for one immutable commit.

## Safety boundary

- QSOs may produce bounded, reviewable payment intents; they cannot approve their own intents.
- External adapters remain disabled until separately authorized, tested, and audited.
- Credentials, private keys, and sensitive account identifiers must not appear in repository records or public artifacts.
- Allocation totals must reconcile under explicit rounding and remainder rules or fail closed.
- Missing evidence remains unresolved rather than being represented as successful settlement.
