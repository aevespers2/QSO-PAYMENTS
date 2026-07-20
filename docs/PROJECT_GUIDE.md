# QSO-PAYMENTS Project Guide

QSO-PAYMENTS defines an audit-first documentation and contract boundary for payment intent in the A.L.I.S.T.A.I.R.E. and Quantum State Object ecosystem. Its first release is deliberately documentation-only: it explains how economic proposals are represented, reviewed, authorized, disputed, and handed to disabled external adapters without implying custody or production settlement capability.

> **Current maturity:** charter candidate. No executable transfer, signing, custody, credential, testnet, or production settlement path is approved.

## Portfolio purpose

A.L.I.S.T.A.I.R.E. is the canonical system objective. QSO-PAYMENTS contributes a bounded economic-intent and evidence layer to that system. It can help autonomous engineering workflows state resource needs, prepare budget and allocation proposals, request independent authorization, and reconcile returned evidence. It is not the autonomous-development control plane and cannot create or inherit financial authority.

This separation allows development automation to accelerate planning and verification without allowing urgency, confidence, repository ownership, QSO identity, or a genome to become permission to move funds.

See [A.L.I.S.T.A.I.R.E. integration](ALISTAIRE_INTEGRATION.md) for the portfolio interfaces, authority matrix, and unresolved ownership decisions.

## Product purpose

QSO-PAYMENTS exists to make economic intent reviewable before any external system is allowed to act. It separates:

- what A.L.I.S.T.A.I.R.E., a QSO, or a human proposes;
- what policy permits;
- what a human or authorized service approves;
- how allocations are calculated;
- what evidence a disabled adapter would require;
- how receipts, disputes, reversals, and reconciliation are represented.

The repository does not provide banking, investment, custody, brokerage, escrow, money-transmission, or guaranteed-return services.

## Authority model

```mermaid
flowchart LR
    Q[A.L.I.S.T.A.I.R.E., QSO, or human proposal] --> I[Payment intent]
    I --> V[Schema and policy validation]
    V -->|invalid or expired| X[Rejected with evidence]
    V -->|valid| H[Independent human or approved-service authorization]
    H -->|not approved| X
    H -->|approved| A[Allocation and route plan]
    A --> D[Disabled settlement adapter boundary]
    D -->|simulation evidence only| R[Receipt or failure record]
    R --> C[Reconciliation and dispute state]
```

A proposal never becomes authorization merely because it is well-formed. Authorization never becomes settlement merely because an allocation is complete. Documentation and fixtures never establish production capability.

## Environment labels

| Environment | Permitted meaning | Prohibited implication |
|---|---|---|
| Documentation | Describes concepts, contracts, risks, and review procedures | A working service exists |
| Simulation | Deterministic local calculations with fictional values and no credentials | Assets can move |
| Testnet | Separately approved integration using non-production networks and isolated credentials | Production readiness |
| Production | Independently authorized, audited, monitored, and legally reviewed deployment | Inferred from any earlier stage |

The current repository release surface is **Documentation** only.

## Contract families

### Payment intent

A bounded proposal should identify purpose, asset or unit, amount, recipients, expiry, provenance, environment, idempotency key, the originating A.L.I.S.T.A.I.R.E. objective or task, and the policy profile under which it may be reviewed.

### Authorization

Authorization is an independent record containing approver identity or role, approved scope, limits, timestamps, conditions, and revocation state. It must never be inferred from QSO identity, prior behavior, autonomous-development status, or a generated recommendation.

### Allocation

Allocation transforms an authorized total into explicit destinations using declared rounding, remainder, cap, and priority rules. Every route must reconcile to the approved total or fail closed.

### Receipt and reconciliation

A receipt records what an external adapter reports, including adapter identity, environment, reference, result, timestamps, hashes, and failure details. Reconciliation compares intent, authorization, allocation, and receipt without rewriting their original records.

### Dispute and rollback

A dispute links contested records, reason codes, evidence, review status, and permitted remediation. Rollback means withdrawing a documentation or simulation candidate, disabling an adapter, revoking credentials, or restoring a prior verified publication artifact; it does not imply reversal is always possible in an external financial network.

## Threat model

QSO-PAYMENTS documentation and future contracts must account for:

- self-approval by a QSO or autonomous-development service;
- forged or replayed authorization;
- ambiguous environment labels;
- allocation totals that do not reconcile;
- rounding or remainder manipulation;
- stale, duplicate, or expired intents;
- adapter substitution and receipt forgery;
- credential leakage or excessive workflow permissions;
- claims that imply custody, legal approval, guaranteed returns, or production capability;
- privacy leakage through payment metadata;
- inaccessible notices or review controls;
- cross-repository authority inheritance that was never explicitly approved.

## Developer onboarding

1. Read `README.md`, `taskchain.md`, `release.md`, and `changelog.md`.
2. Read the A.L.I.S.T.A.I.R.E. integration boundary before describing any portfolio dependency.
3. Treat P0 charter approval as a hard gate; documentation may be refined, but approval must not be invented.
4. Keep all current examples fictional, deterministic, and credential-free.
5. Label every capability statement as documentation, simulation, testnet, or production.
6. Separate intent, authorization, allocation, adapter, receipt, dispute, and reconciliation records.
7. Add positive and negative fixtures before proposing executable schemas.
8. Record exact publication commands, workflow versions, link/accessibility/security results, artifact hashes, and rollback evidence.

See [Developer onboarding](ONBOARDING.md) for the local build and pull-request workflow.

## Documentation release gates

The first documentation candidate is not ready until:

- the payment-boundary charter is approved;
- the A.L.I.S.T.A.I.R.E. subsystem role and control-plane separation are approved;
- terminology, users, jurisdictions, privacy assumptions, license, review ownership, and prohibited capabilities are explicit;
- the Pages artifact is reproducible from one immutable commit;
- links, HTML, accessibility, claims, privacy, security, and workflow permissions are reviewed;
- checksums, provenance, and rollback instructions are retained;
- no page implies production custody, signing, settlement, investment returns, or autonomous transfers.

## Documentation map

- [Public project page](index.md)
- [Architecture and trust boundaries](ARCHITECTURE.md)
- [A.L.I.S.T.A.I.R.E. integration](ALISTAIRE_INTEGRATION.md)
- [Design contracts](DESIGN_CONTRACTS.md)
- [Developer onboarding](ONBOARDING.md)
- [Security and privacy](SECURITY_PRIVACY.md)
- [Operations and recovery](OPERATIONS.md)
- [Documentation-only decision](decisions/0001-documentation-only-boundary.md)
- [Task chain](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/taskchain.md)
- [Release plan](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/release.md)
- [Changelog](https://github.com/aevespers2/QSO-PAYMENTS/blob/main/changelog.md)
- [Repository overview](https://github.com/aevespers2/QSO-PAYMENTS#readme)
