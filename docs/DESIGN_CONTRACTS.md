# Design contracts

This document defines the **proposed semantics** that later schemas and simulation fixtures must preserve. It is not an executable API specification and does not authorize adapters, credentials, custody, signing, or transfers.

## Record families

Every record is immutable after acceptance. Corrections and state transitions create linked records rather than silently rewriting prior evidence.

| Record | Purpose | Minimum relationships |
|---|---|---|
| Payment intent | Express a bounded economic proposal | proposer, policy profile, environment, expiry, idempotency key |
| Validation result | Record schema and policy evaluation | intent, validator version, findings, timestamp |
| Authorization | Approve or deny a defined scope | intent, approver role, limits, conditions, expiry, revocation state |
| Allocation | Resolve an approved total into explicit routes | authorization, rounding rule, remainder rule, route totals |
| Adapter submission | Describe a separately authorized handoff | allocation, adapter version, environment, request digest |
| Receipt or failure | Preserve what the adapter reported | submission, adapter reference, status, timestamps, evidence digest |
| Reconciliation | Compare expected and reported outcomes | allocation, receipt or failure, differences, review state |
| Dispute | Contest one or more records without deleting them | linked evidence, reason, reviewer, status, remediation decision |

## Common envelope

A future schema should use an explicit envelope rather than relying on filenames, transport metadata, or database context.

```yaml
record_type: payment_intent
schema_version: qso-payments/0.x
record_id: immutable-unique-id
created_at: RFC3339 timestamp
created_by:
  subject_id: pseudonymous-or-approved-identifier
  subject_type: qso | human | service
  role: proposer
context:
  environment: simulation
  correlation_id: immutable-workflow-id
  idempotency_key: bounded-retry-key
provenance:
  predecessor_ids: []
  content_digest: sha256:...
  producer_version: ...
classification: public-fixture | internal | sensitive | secret-prohibited
payload: {}
```

The field names are illustrative until a separate schema decision is approved. The semantic requirements are binding documentation constraints for future design work.

## Payment-intent semantics

A payment intent should state:

- purpose and human-readable rationale;
- asset, currency, or simulation unit;
- approved precision and amount representation;
- intended recipients or allocation policy reference;
- earliest and latest valid execution times;
- environment and jurisdictional assumptions;
- provenance and policy profile;
- idempotency key and replay window;
- data classification and retention class;
- explicit statement that the record is a proposal, not authority.

An intent fails closed when required fields are absent, the environment is ambiguous, the intent is expired, a duplicate idempotency key conflicts with prior content, the requested route is prohibited, or policy evidence is unavailable.

## Authorization semantics

Authorization must be independent from the proposer and must never be inferred from QSO identity, reputation, prior approvals, or successful validation. It records:

- approving subject or approved service role;
- exact intent digest and schema version;
- approved amount, routes, limits, and environment;
- conditions, expiry, and revocation state;
- policy and evidence references;
- decision reason and timestamp.

Any material change to amount, recipient, route, adapter, environment, or policy requires a new authorization.

## Allocation and arithmetic

Amounts should use integer minor units or an explicitly defined fixed-precision representation. Floating-point values are not acceptable for authoritative accounting records.

For every allocation:

```text
sum(route amounts) + declared remainder = authorized total
```

The design must define deterministic ordering, caps, floors, percentage precision, rounding direction, remainder ownership, and behavior when a recipient is ineligible. Any unresolved mismatch produces a failure record and no adapter handoff.

## State transitions

```text
PROPOSED
  -> REJECTED
  -> AWAITING_AUTHORIZATION
       -> REJECTED
       -> AUTHORIZED
            -> ALLOCATION_FAILED
            -> ALLOCATED
                 -> ADAPTER_HELD
                 -> SIMULATION_RECORDED
                 -> SUBMITTED        [separate approval only]
                      -> RECEIPT_RECORDED
                           -> RECONCILED
                           -> DISPUTED
```

Transitions are append-only, attributable, and environment-specific. A later dispute does not erase an earlier receipt or reconciliation record.

## Idempotency, retries, and partial failure

- The same idempotency key and identical content return the existing workflow identity.
- The same idempotency key with different content fails as a conflict.
- Retry budgets are finite and recorded.
- Timeouts remain unknown until reconciliation resolves them.
- Partial route outcomes are represented route by route; they are never collapsed into an unqualified success.
- A retry may not duplicate a route already evidenced as accepted by an external system.

## Receipt and finality language

A receipt is evidence that a named adapter reported a result at a given time. It is not automatically proof of legal finality, irreversibility, funds availability, counterparty identity, or completion across every downstream system. Documentation must name the finality assumptions and unresolved states for each future adapter.

## Compatibility and migration

A later executable contract requires:

1. versioned schemas with stable identifiers;
2. deterministic canonicalization and digest rules;
3. forward and backward compatibility statements;
4. migration fixtures for every supported transition;
5. rejection behavior for unknown fields and unsupported versions;
6. retained evidence linking source and migrated records;
7. a rollback plan that never depends on deleting accepted evidence.

No compatibility promise exists until those artifacts and tests are approved.
