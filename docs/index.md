# QSO-PAYMENTS

**Auditable economic intent without uncontrolled custody.**

QSO-PAYMENTS is A.L.I.S.T.A.I.R.E.'s bounded economic-intent, allocation-preview, evidence, dispute, and reconciliation subsystem. It documents the boundary between a resource proposal and any external system that could move assets. The current release surface is documentation only: it defines responsibilities, records, evidence, compatibility witnesses, and review gates without providing custody, signing, credentials, testnet execution, production settlement, investment products, or guaranteed returns.

!!! warning "Current maturity"
    This repository is a charter and contract-design candidate. Documentation may explain a future interface, but it does not establish that the interface exists, is authorized, is financially approved, or is suitable for production use.

## A.L.I.S.T.A.I.R.E. role

Repository `0` may identify a resource need, prepare a bounded local proposal, compare fictional or externally supplied options, and assemble evidence. QSO-PAYMENTS may validate and transform that proposal into a reviewable economic intent. Neither may approve, fund, sign, custody, or settle the request.

An independent human or separately approved financial authority must issue an attributable financial authorization. Repository `1` may later admit and record a narrower execution capability after verifying that authorization, but a generic capability cannot substitute for financial approval. External adapters remain disabled.

See [A.L.I.S.T.A.I.R.E. integration](ALISTAIRE_INTEGRATION.md) and the [obstruction and gluing analysis](OBSTRUCTION_AND_GLUING.md).

## Authority model

```mermaid
flowchart LR
    R0["Repository 0\nlocal resource proposal"] --> I["QSO-PAYMENTS\nvalidated economic intent"]
    I --> S["Approved review surface"]
    S --> F["Independent financial authorization"]
    F --> R1["Repository 1\nnarrow capability admission"]
    R1 --> G["External adapter gate\ndisabled by default"]
    G -. "separately approved environment only" .-> X["External payment system"]
    G --> E["Held, simulated, failed, or unknown evidence"]
    X -. "adapter-reported evidence" .-> E
    E --> C["QSO-PAYMENTS reconciliation"]
    C --> D["Repository 1 canonical disposition"]
```

A proposal is not validation. Validation is not financial approval. Financial approval is not a reusable credential. A capability is not approval. Adapter execution is not canonical acceptance or legal finality. Reconciliation preserves uncertainty and correction history.

## Current product boundary

| Area | Current status | Meaning |
|---|---|---|
| Documentation | In scope | Architecture, terminology, trust boundaries, gluing contracts, review procedures, and release evidence |
| Simulation | Not yet approved | Future deterministic calculations using fictional values and no external credentials |
| Testnet | Not authorized | Requires separate schemas, isolated credentials, legal/security/privacy review, monitoring, emergency stop, and human approval |
| Production | Prohibited by current scope | Cannot be inferred from schemas, fixtures, documentation, simulation, or testnet activity |

## Core guarantees

1. A QSO, Repository `0`, QSO-PAYMENTS, or interface cannot approve its own payment intent.
2. Financial authorization is explicit, attributable, scoped, revocable, environment-specific, and distinct from generic capability issuance.
3. Repository `1` cannot broaden amount, destination, environment, duration, adapter, or policy scope.
4. Allocation routes must reconcile exactly under declared unit, precision, rounding, fee, tax, and remainder rules.
5. Credentials, private keys, complete account identifiers, and sensitive financial data never belong in public records, QSO state, model context, repository fixtures, or Pages artifacts.
6. Adapters remain disabled unless a separately approved release activates a named version and environment.
7. Original proposal, intent, authorization, capability, execution evidence, receipt, dispute, correction, and reconciliation records remain linked and append-only.
8. Pending, unknown, contradictory, reversed, disputed, or unresolved status is preserved rather than presented as successful settlement.
9. Repository, QSO, genome, task, interface, workflow, or transported-message identity never implies financial capability.
10. Revocation, correction, emergency stop, evidence preservation, cache invalidation, and bounded recovery must glue across every participating component.

## Material obstruction

The portfolio has not yet adopted one jointly versioned contract separating independent financial approval from Repository `1` capability admission. Without that distinction, a technical permission could be misrepresented as authority to spend, or adapter success could be misrepresented as final settlement. The [obstruction and gluing analysis](OBSTRUCTION_AND_GLUING.md) records 18 active incompatibilities and the pairwise and triple-overlap witnesses required to resolve them.

## Documentation map

- [Project guide](PROJECT_GUIDE.md): purpose, terminology, contract families, threats, and release gates.
- [Architecture](ARCHITECTURE.md): trust boundaries, lifecycle, data classes, dependencies, and verification strategy.
- [A.L.I.S.T.A.I.R.E. integration](ALISTAIRE_INTEGRATION.md): subsystem role, portfolio interfaces, authority matrix, autonomous-evolution limits, and ownership decisions.
- [Obstruction and gluing analysis](OBSTRUCTION_AND_GLUING.md): active compatibility failures, pairwise contracts, triple-overlap witnesses, result semantics, and acceptance order.
- [Design contracts](DESIGN_CONTRACTS.md): proposed record semantics, invariants, failure modes, and compatibility rules.
- [Developer onboarding](ONBOARDING.md): local documentation setup, contribution workflow, and review checklist.
- [Security and privacy](SECURITY_PRIVACY.md): threat model, data minimization, secret handling, and claims controls.
- [Operations and recovery](OPERATIONS.md): evidence retention, incident response, emergency disable, recovery, and rollback.
- [ADR-0001](decisions/0001-documentation-only-boundary.md): why the first release is documentation-only.

## Release posture

The release remains blocked until the payment charter, financial authority, Repository `1` role, contract owner, identity namespaces, compatibility witnesses, privacy and retention model, and recovery owners are approved. The current exact head must also pass reproducible strict documentation validation, accessibility and claims review, independent security/privacy review, checksum and provenance retention, separately authorized publication verification, and rollback evidence. See the repository [task chain](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/taskchain.md), [punch list](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/punchlist.md), [release plan](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/release.md), and [changelog](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/changelog.md).
