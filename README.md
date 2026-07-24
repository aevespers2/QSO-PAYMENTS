# QSO-PAYMENTS

Auditable payment-intent, authorization, allocation, receipt, dispute, reconciliation, and disabled settlement-adapter boundaries for the A.L.I.S.T.A.I.R.E. and Quantum State Object ecosystem.

> **Current release surface: documentation only.** QSO-PAYMENTS does not custody assets, sign transactions, hold credentials, execute testnet or production transfers, provide investment products, or promise returns.

## A.L.I.S.T.A.I.R.E. role

A.L.I.S.T.A.I.R.E. is the canonical system objective. QSO-PAYMENTS is its bounded **economic-intent, allocation-preview, evidence, dispute, and reconciliation subsystem**. It is not Repository `0`, Repository `1`, a financial approver, a credential store, a custodian, or a payment processor.

The current lowest-coupling route is:

```text
Repository 0 local resource proposal
→ QSO-PAYMENTS validated economic intent
→ QSO-STUDIO or another approved review surface
→ independent financial authorization
→ Repository 1 admission and narrow execution capability
→ disabled external adapter boundary
→ execution evidence
→ QSO-PAYMENTS reconciliation
→ Repository 1 canonical disposition
```

Repository `0` may propose and verify resource needs but cannot approve or fund them. Repository `1` may become the generic capability and canonical-state authority after approval, but a generic capability cannot substitute for an independent financial authorization. Adapter execution is evidence, not automatic canonical or legal finality.

## Documentation

- [GitHub Pages source](docs/index.md)
- [Project guide](docs/PROJECT_GUIDE.md)
- [Architecture and trust boundaries](docs/ARCHITECTURE.md)
- [A.L.I.S.T.A.I.R.E. integration](docs/ALISTAIRE_INTEGRATION.md)
- [Portable trust and financial authority](docs/PORTABLE_TRUST_FINANCIAL_BOUNDARY.md)
- [Obstruction and gluing analysis](docs/OBSTRUCTION_AND_GLUING.md)
- [Design contracts](docs/DESIGN_CONTRACTS.md)
- [Contract and interface reference](docs/CONTRACT_REFERENCE.md)
- [Independent financial authorization review](docs/FINANCIAL_AUTHORIZATION_REVIEW.md)
- [Status, finality, and correction lifecycle](docs/STATUS_FINALITY_LIFECYCLE.md)
- [Developer onboarding](docs/ONBOARDING.md)
- [Accessibility and plain-language review](docs/ACCESSIBILITY_REVIEW.md)
- [Security and privacy](docs/SECURITY_PRIVACY.md)
- [Operations and recovery](docs/OPERATIONS.md)
- [Architecture decision](docs/decisions/0001-documentation-only-boundary.md)
- [Task chain](taskchain.md)
- [Punch list](punchlist.md)
- [Release plan](release.md)
- [Changelog](changelog.md)

## Product boundary

```text
A.L.I.S.T.A.I.R.E. objective or bounded human/QSO proposal
→ payment intent
→ schema and policy validation
→ independent financial authorization
→ narrow capability admission
→ deterministic allocation and reconciliation
→ disabled external-adapter boundary
→ receipt, failure, pending, unknown, reversal, or dispute evidence
```

A proposal is not authorization. Financial authorization is not a reusable credential. A generic capability is not financial approval. Authorization is not settlement. A receipt is adapter-reported evidence, not an unconditional claim of finality. Documentation and simulation evidence do not establish production capability.

QSO-PAYMENTS documents three independent status dimensions: **processing**, **authority**, and **evidence/finality**. Technical completion cannot create financial approval; adapter-reported success cannot create canonical acceptance; canonical acceptance cannot silently establish jurisdiction-dependent legal finality. Corrections, revocations, reversals, disputes, and unknown outcomes remain linked and visible.

## Environment model

- **Documentation — current:** concepts, contracts, risks, review procedures, gluing requirements, accessibility requirements, and publication evidence.
- **Simulation — future approval:** deterministic fictional calculations with no credentials, custody, signing, or external transfers.
- **Testnet — not authorized:** separately governed non-production integration with explicit human approval and isolated credentials.
- **Production — prohibited by current scope:** independently authorized, audited, monitored, legally reviewed deployment with tested emergency stop and recovery.

Only the documentation environment is currently in release scope.

## Build the documentation

```bash
python -m venv .venv
. .venv/bin/activate
python -m pip install -r requirements-docs.txt
mkdocs build --strict
```

The validation workflow builds the pinned MkDocs site, asserts the submitted source identity, checks generated-site boundaries, produces SHA-256 evidence, and retains review artifacts. It does not publish Pages, activate adapters, or approve a release. A successful build is verification input only.

## Safety boundary

- QSOs and Repository `0` workflows may produce bounded, reviewable payment intents; they cannot approve their own intents.
- Independent financial authorization must be attributable, exactly scoped, time-bounded, revocable, correction-linked, and separately governed; a review record cannot create authority merely by being complete or well formatted.
- Repository `1` cannot invent financial approval or broaden an accepted amount, destination, environment, duration, or adapter scope.
- External adapters remain disabled until separately authorized, tested, audited, legally reviewed, and operationally governed.
- Credentials, private keys, complete account identifiers, and sensitive payment data must not appear in repository records, fixtures, logs, model context, or public artifacts.
- Allocation totals must reconcile under explicit fixed-precision, rounding, fee, tax, and remainder rules or fail closed.
- Retries require shared idempotency and replay domains and cannot duplicate a previously accepted route.
- Missing, stale, contradictory, partial, or unverifiable evidence remains `PENDING`, `UNKNOWN`, `DISPUTED`, or another explicit non-success state.
- A `COMPLETED` processing stage, `AUTHORIZED` decision, `ADAPTER_REPORTED` outcome, `RECONCILED` result, canonical disposition, and legal finality are different claims and must never be collapsed.
- Revocation, correction, emergency stop, evidence preservation, cache invalidation, and bounded recovery must work across every participating repository.
- Status, authority, environment, and finality distinctions must remain understandable without color, diagrams, or portfolio-specific shorthand.
- No documentation page constitutes a financial product, custody service, settlement service, legal certification, suitability determination, or promise of returns.
