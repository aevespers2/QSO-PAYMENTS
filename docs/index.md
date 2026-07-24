# QSO-PAYMENTS

**Auditable economic intent without uncontrolled custody.**

QSO-PAYMENTS is A.L.I.S.T.A.I.R.E.'s bounded economic-intent, allocation-preview, evidence, dispute, and reconciliation subsystem. It documents the boundary between a resource proposal and any external system that could move assets. The current release surface is documentation only: it defines responsibilities, records, evidence, compatibility witnesses, accessibility requirements, and review gates without providing custody, signing, credentials, testnet execution, production settlement, investment products, or guaranteed returns.

!!! warning "Current maturity"
    This repository is a charter and contract-design candidate. Documentation may explain a future interface, but it does not establish that the interface exists, is authorized, is financially approved, or is suitable for production use.

## A.L.I.S.T.A.I.R.E. role

Repository `0` may identify a resource need, prepare a bounded local proposal, compare fictional or externally supplied options, and assemble evidence. QSO-PAYMENTS may validate and transform that proposal into a reviewable economic intent. Neither may approve, fund, sign, custody, or settle the request.

An independent human or separately approved financial authority must issue an attributable financial authorization. Repository `1` may later admit and record a narrower execution capability after verifying that authorization, but a generic capability cannot substitute for financial approval. External adapters remain disabled.

See [A.L.I.S.T.A.I.R.E. integration](ALISTAIRE_INTEGRATION.md), the [contract and interface reference](CONTRACT_REFERENCE.md), the [independent financial authorization review guide](FINANCIAL_AUTHORIZATION_REVIEW.md), the [status, finality, and correction lifecycle](STATUS_FINALITY_LIFECYCLE.md), and the [obstruction and gluing analysis](OBSTRUCTION_AND_GLUING.md).

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

**Equivalent prose:** Repository `0` may create a local resource proposal, which QSO-PAYMENTS may convert into a validated economic intent. An approved review surface presents that intent to an independent financial authority. Only after independent authorization may Repository `1` admit a narrower technical capability. The external adapter gate remains disabled by default and can reach an external system only through a separately approved environment. Held, simulated, failed, pending, partial, or unknown evidence returns to QSO-PAYMENTS for reconciliation before Repository `1` or an approved successor records a canonical disposition. No step inherits the authority of the step before it.

A proposal is not validation. Validation is not financial approval. Financial approval is not a reusable credential. A capability is not approval. Adapter execution is not canonical acceptance or legal finality. Reconciliation preserves uncertainty and correction history.

## Status and finality model

Future records must preserve three independent dimensions rather than compressing all meaning into one `status` field:

1. **Processing status** — where a bounded technical stage is in its workflow.
2. **Authority status** — whether an approved independent authority issued an exact decision.
3. **Evidence/finality status** — what execution evidence exists and whether it has been reconciled or independently accepted.

A completed processing stage is not authorization. An authorization is not a credential or execution result. Adapter-reported success is not reconciliation, canonical acceptance, or legal finality. Partial, unknown, disputed, reversed, corrected, expired, revoked, superseded, and withdrawn states remain first-class and visible.

## Current product boundary

| Area | Current status | Meaning |
|---|---|---|
| Documentation | In scope | Architecture, terminology, trust boundaries, gluing contracts, accessible status semantics, authorization-review procedure, lifecycle/finality distinctions, and release evidence |
| Simulation | Not yet approved | Future deterministic calculations using fictional values and no external credentials |
| Testnet | Not authorized | Requires separate schemas, isolated credentials, legal/security/privacy review, monitoring, emergency stop, and human approval |
| Production | Prohibited by current scope | Cannot be inferred from schemas, fixtures, documentation, simulation, or testnet activity |

## Core guarantees

1. A QSO, Repository `0`, QSO-PAYMENTS, or interface cannot approve its own payment intent.
2. Financial authorization is explicit, attributable, scoped, revocable, environment-specific, correction-linked, and distinct from generic capability issuance.
3. A review record remains `DOCUMENTED_NOT_AUTHORIZED` unless a separately designated human authority issues an exact decision under approved policy; completeness, formatting, or workflow success cannot create authority.
4. Repository `1` cannot broaden amount, destination, environment, duration, adapter, or policy scope.
5. Allocation routes must reconcile exactly under declared unit, precision, rounding, fee, tax, and remainder rules.
6. Credentials, private keys, complete account identifiers, and sensitive financial data never belong in public records, QSO state, model context, repository fixtures, or Pages artifacts.
7. Adapters remain disabled unless a separately approved release activates a named version and environment.
8. Original proposal, intent, authorization, capability, execution evidence, receipt, dispute, correction, and reconciliation records remain linked and append-only.
9. Pending, unknown, contradictory, reversed, disputed, or unresolved status is preserved rather than presented as successful settlement.
10. Repository, QSO, genome, task, interface, workflow, or transported-message identity never implies financial capability.
11. Revocation, correction, emergency stop, evidence preservation, cache invalidation, and bounded recovery must glue across every participating component.
12. Status, authority, environment, and finality distinctions must be expressed in text and remain understandable without color or diagrams.
13. `COMPLETED`, `AUTHORIZED`, `ADAPTER_REPORTED`, `RECONCILED`, `CANONICALLY_ACCEPTED`, and legal finality are distinct claims with separate owners and evidence requirements.
14. Corrections, revocations, reversals, disputes, and superseding records never delete or silently rewrite the prior generation.

## Material obstruction

The portfolio has not yet adopted one jointly versioned contract separating independent financial approval from Repository `1` capability admission. It also lacks an approved independent authorizer, authority-source model, exact review-record profile, canonical multi-dimensional status registry, transition owner, consumer-notification topology, and correction/revocation owner. Without those boundaries, a technical permission or complete review form could be misrepresented as authority to spend, or adapter success could be misrepresented as final settlement. The [obstruction and gluing analysis](OBSTRUCTION_AND_GLUING.md) records 18 active incompatibilities and the pairwise and triple-overlap witnesses required to resolve them.

## Documentation map

- [Project guide](PROJECT_GUIDE.md): purpose, terminology, contract families, threats, and release gates.
- [Architecture](ARCHITECTURE.md): trust boundaries, lifecycle, data classes, dependencies, and verification strategy.
- [A.L.I.S.T.A.I.R.E. integration](ALISTAIRE_INTEGRATION.md): subsystem role, portfolio interfaces, authority matrix, autonomous-evolution limits, and ownership decisions.
- [Portable trust and financial authority](PORTABLE_TRUST_FINANCIAL_BOUNDARY.md): device/workspace bindings, independent financial approval, revocation, stop domains, and recovery.
- [Obstruction and gluing analysis](OBSTRUCTION_AND_GLUING.md): active compatibility failures, pairwise contracts, triple-overlap witnesses, result semantics, and acceptance order.
- [Design contracts](DESIGN_CONTRACTS.md): proposed record semantics, invariants, failure modes, and compatibility rules.
- [Contract and interface reference](CONTRACT_REFERENCE.md): conceptual interface surfaces, record families, envelope, statuses, reason codes, examples, migration, and authority limits.
- [Independent financial authorization review](FINANCIAL_AUTHORIZATION_REVIEW.md): role separation, decision states, exact bindings, evidence package, fail-closed stops, correction and revocation, gluing witnesses, and reviewer onboarding.
- [Status, finality, and correction lifecycle](STATUS_FINALITY_LIFECYCLE.md): three-dimensional status semantics, transition constraints, partial/unknown outcomes, correction closure, accessible rendering, and reviewer onboarding.
- [Developer onboarding](ONBOARDING.md): local documentation setup, contribution workflow, and review checklist.
- [Accessibility and plain-language review](ACCESSIBILITY_REVIEW.md): text-equivalent status semantics, diagram alternatives, navigation, keyboard, zoom, and comprehension review.
- [Security and privacy](SECURITY_PRIVACY.md): threat model, data minimization, secret handling, and claims controls.
- [Operations and recovery](OPERATIONS.md): evidence retention, incident response, emergency disable, recovery, and rollback.
- [ADR-0001](decisions/0001-documentation-only-boundary.md): why the first release is documentation-only.

## Release posture

The release remains blocked until the payment charter, financial authority, Repository `1` role, contract owner, identity namespaces, status and transition ownership, compatibility witnesses, privacy and retention model, and recovery owners are approved. The current exact head must also pass reproducible strict documentation validation, financial-authorization-record review, lifecycle/finality review, accessibility and claims review, independent security/privacy review, checksum and provenance retention, separately authorized publication verification, and rollback evidence. See the repository [task chain](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/taskchain.md), [punch list](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/punchlist.md), [release plan](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/release.md), and [changelog](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/changelog.md).
