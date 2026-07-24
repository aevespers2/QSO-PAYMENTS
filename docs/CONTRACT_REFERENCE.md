# Contract and interface reference

Status: **proposed documentation-only reference**

This reference organizes the record families and interface boundaries that a future simulation-only QSO-PAYMENTS contract package would need to define. It is not an executable API, schema release, financial authorization service, adapter specification, or promise of compatibility.

## Reading rule

Every example below is illustrative. Field names, namespaces, canonical bytes, signatures, reason codes, and version identifiers remain unapproved until a separately governed contract package is selected and reviewed.

```text
proposal != validation
validation != financial authorization
financial authorization != generic capability
capability != adapter execution
adapter execution != receipt truth
receipt != reconciliation
reconciliation != legal or canonical finality
```

## Interface surfaces

| Surface | Producer | Consumer | Required boundary | Current disposition |
|---|---|---|---|---|
| Resource proposal | Repository `0` or approved human workflow | QSO-PAYMENTS | Proposal contains no self-approval or funding authority | Documentation candidate |
| Economic intent | QSO-PAYMENTS | Approved review surface | Exact proposal lineage, environment, amount representation, purpose, expiry, and policy profile | Documentation candidate |
| Financial authorization | Independent financial authority | Repository `1` and QSO-PAYMENTS | Independent approval, limits, conditions, expiry, revocation, and exact intent digest | Owner unresolved |
| Capability admission | Repository `1` or approved successor | Disabled adapter boundary | Narrower than authorization; bound to device, workspace, repository, environment, and adapter | Owner unresolved |
| Adapter submission | Separately approved adapter controller | External system | Credentials and signing remain outside QSO-PAYMENTS; request digest and idempotency are explicit | Disabled |
| Adapter evidence | Adapter controller | QSO-PAYMENTS | Raw response identity, uncertainty, environment, timestamps, and redaction declaration | Documentation candidate |
| Reconciliation | QSO-PAYMENTS | Repository `1` and human review | Expected-versus-observed differences and unresolved status remain explicit | Documentation candidate |
| Canonical disposition | Repository `1` or approved successor | Portfolio consumers | Must not infer legal finality or settlement solely from adapter evidence | Owner unresolved |

## Common envelope

A future record should carry an explicit envelope so meaning does not depend upon a file name, queue, database table, or transport path.

```yaml
profile_id: qso-payments/<approved-profile>
profile_version: <immutable-version>
record_type: payment_intent
record_id: <immutable-unique-id>
created_at: <RFC3339-with-timezone>
created_by:
  subject_id: <approved-pseudonymous-or-service-id>
  subject_type: human | qso | service
  role: proposer
context:
  environment: simulation
  correlation_id: <immutable-workflow-id>
  idempotency_key: <bounded-retry-domain-key>
  device_id: <optional-approved-device-id>
  workspace_id: <optional-approved-workspace-id>
  repository: <optional-owner/name>
  expected_head: <optional-40-character-git-sha>
provenance:
  predecessor_ids: []
  source_digest: sha256:<hex>
  canonical_digest: sha256:<hex>
  producer_version: <immutable-producer-version>
classification: public-fixture | internal | sensitive | secret-prohibited
payload: {}
```

The envelope must fail closed when the profile is unknown, identity fields are malformed, environment is absent, a required predecessor is missing, a digest does not match, time lacks a timezone, or an optional execution binding is required but omitted.

## Record-family reference

### `resource_proposal`

Purpose: express a bounded resource need without creating payment authority.

Required semantics:

- proposer identity and authority source;
- purpose, beneficiary, evidence, and alternatives;
- maximum requested amount or explicit unknown amount;
- environment and jurisdictional assumptions;
- expiration and correction route;
- explicit `authority_effect: none`.

### `payment_intent`

Purpose: transform an accepted proposal into a precise review object.

Required semantics:

- exact proposal identifier and digest;
- asset or fictional simulation unit;
- integer minor units or an approved fixed-precision representation;
- requested destinations or allocation policy;
- earliest and latest valid times;
- policy, privacy, retention, and evidence references;
- idempotency and replay domain;
- explicit statement that the intent is not authorization.

### `validation_result`

Purpose: record structural and policy evaluation without approving spending.

Required semantics:

- exact intent digest and validator generation;
- deterministic findings and reason codes;
- observed versus inferred fields;
- `VALID`, `INVALID`, or `INDETERMINATE` result;
- no authority promotion from `VALID`.

### `financial_authorization`

Purpose: approve or deny one exact economic scope through an independent authority.

Required semantics:

- exact intent digest;
- authorizer identity, role, and authority source;
- amount, destination, environment, adapter, and duration limits;
- conditions, expiry, revocation state, and reason;
- separation from the proposer, validator, and generic capability issuer.

Any material change requires a new authorization. Prior authorization cannot be silently edited or broadened.

### `allocation_plan`

Purpose: divide an authorized total into deterministic routes.

Required semantics:

```text
sum(route amounts) + declared remainder = authorized total
```

The contract must define ordering, precision, rounding direction, caps, floors, fees, taxes, remainder ownership, ineligible recipients, and failure behavior. Floating-point arithmetic is not acceptable for authoritative amounts.

### `capability_admission`

Purpose: allow a narrowly scoped technical action after independent financial authorization.

Required semantics:

- authorization identifier and digest;
- action class, adapter, environment, and expiry;
- device, enrollment generation, workspace, repository, base commit, and expected head when execution depends on them;
- scope intersection rather than scope union;
- revocation and emergency-stop bindings;
- explicit statement that capability admission is not financial approval.

### `adapter_submission`

Purpose: record a separately authorized attempt to hand an allocation to a named adapter.

Required semantics:

- exact allocation and capability bindings;
- adapter identity and version;
- request digest and redaction declaration;
- idempotency key and retry budget;
- submission time and environment;
- no secret or credential material in public evidence.

### `adapter_evidence`

Purpose: preserve what a named adapter reported.

Allowed states include:

- `HELD`
- `SIMULATED`
- `SUBMITTED`
- `PENDING`
- `FAILED`
- `UNKNOWN`
- `PARTIAL`
- `REVERSED`

An adapter report is evidence, not automatic proof of funds availability, counterparty identity, irreversibility, legal settlement, or canonical completion.

### `reconciliation_result`

Purpose: compare authorized and expected outcomes with adapter-reported evidence.

Required semantics:

- route-by-route expected and observed state;
- differences, uncertainty, missing evidence, and stale evidence;
- duplicate and replay analysis;
- dispute, correction, reversal, and compensation links;
- explicit finality assumptions;
- `RECONCILED`, `DISPUTED`, `INCOMPLETE`, or `UNKNOWN` disposition.

### `dispute_record`

Purpose: challenge one or more records without deleting history.

Required semantics:

- disputed record identifiers;
- claimant, reason, evidence, and requested remedy;
- reviewer and conflict-of-interest state;
- status, correction, reversal, or compensation decision;
- append-only resolution history.

## Status vocabulary

Status labels must appear as text and may not rely on color alone.

| Status | Meaning | Forbidden interpretation |
|---|---|---|
| `PROPOSED` | A request exists | Approved or funded |
| `VALID` | Structure/policy evaluation passed | Financially authorized |
| `AUTHORIZED` | Independent financial scope approved | Executed or settled |
| `ADMITTED` | Technical capability admitted | Financial authority created |
| `HELD` | Adapter action intentionally not attempted | Failed or completed |
| `SIMULATED` | Fictional deterministic result recorded | Testnet or production transfer |
| `SUBMITTED` | Adapter reports request submission | Final, irreversible, or successful |
| `PENDING` | Outcome unresolved | Successful |
| `FAILED` | Named attempt failed | No external side effect necessarily occurred |
| `UNKNOWN` | Evidence is insufficient | Success or failure |
| `PARTIAL` | Routes differ or only some completed | Global success |
| `DISPUTED` | Outcome or evidence is contested | Corrected or reversed |
| `REVERSED` | A later event counteracted an earlier outcome | Original evidence erased |
| `RECONCILED` | Expected and observed records agree under stated assumptions | Legal finality in every system |
| `SUPERSEDED` | A newer record replaces current use | Historical deletion |
| `REVOKED` | Authority or capability is no longer usable | Prior evidence removed |

## Failure and reason-code model

A future reason-code registry should be closed and versioned. Candidate classes include:

- `PROFILE_UNSUPPORTED`
- `SCHEMA_INVALID`
- `IDENTITY_INVALID`
- `DIGEST_MISMATCH`
- `ENVIRONMENT_AMBIGUOUS`
- `EXPIRED`
- `NOT_YET_VALID`
- `AUTHORIZATION_MISSING`
- `AUTHORIZATION_SCOPE_MISMATCH`
- `AUTHORIZATION_REVOKED`
- `CAPABILITY_MISSING`
- `CAPABILITY_SCOPE_MISMATCH`
- `DEVICE_BINDING_MISMATCH`
- `WORKSPACE_BINDING_MISMATCH`
- `EXPECTED_HEAD_MISMATCH`
- `ADAPTER_DISABLED`
- `IDEMPOTENCY_CONFLICT`
- `REPLAY_DETECTED`
- `ALLOCATION_MISMATCH`
- `EVIDENCE_INCOMPLETE`
- `FINALITY_UNKNOWN`
- `CORRECTION_REQUIRED`
- `RECOVERY_BLOCKED`

Unknown reason codes must not be silently treated as warnings or success.

## Example: documentation-only simulation intent

```json
{
  "profile_id": "qso-payments/example-only",
  "profile_version": "0.0.0-documentation",
  "record_type": "payment_intent",
  "record_id": "example-intent-001",
  "created_at": "2026-07-23T15:00:00Z",
  "created_by": {
    "subject_id": "fixture-proposer",
    "subject_type": "human",
    "role": "proposer"
  },
  "context": {
    "environment": "simulation",
    "correlation_id": "example-workflow-001",
    "idempotency_key": "example-idempotency-001"
  },
  "provenance": {
    "predecessor_ids": ["example-proposal-001"],
    "source_digest": "sha256:example-only-not-valid",
    "canonical_digest": "sha256:example-only-not-valid",
    "producer_version": "documentation"
  },
  "classification": "public-fixture",
  "payload": {
    "purpose": "Demonstrate documentation structure only",
    "unit": "fictional-credit",
    "amount_minor": 1000,
    "authority_effect": "none"
  }
}
```

This example is intentionally non-executable and contains invalid placeholder digests so it cannot be mistaken for an accepted contract fixture.

## Compatibility and migration requirements

No compatibility claim exists until all of the following are approved and evidenced:

1. immutable schema and semantic profile identifiers;
2. canonical byte and digest rules;
3. closed reason-code and status registries;
4. producer and consumer registrations;
5. positive, negative, stale, replay, duplicate, wrong-device, wrong-workspace, wrong-head, partial-failure, correction, revocation, and recovery fixtures;
6. direct and chained migration equivalence;
7. lossy-field declarations that cannot broaden authority;
8. dual-read or dual-write reconciliation rules where applicable;
9. consumer acknowledgment and rollback closure;
10. retained source, workflow, artifact, and expiration evidence.

## Accessibility and review requirements

- Every state and decision must be readable as text without color, icon, or diagram position.
- Tables require clear headers and must remain understandable when read linearly.
- Diagrams require equivalent prose.
- Examples must visibly distinguish fictional fixtures from executable records.
- Warnings about authority, finality, privacy, and environment must appear before procedural details.
- Public documentation must not include credentials, complete account identifiers, private device identifiers, or sensitive payment evidence.

See the [accessibility review guide](ACCESSIBILITY_REVIEW.md) for the documentation acceptance checklist.

## Authority boundary

This document creates no schema, API, registry, credential, financial approval, capability, adapter admission, custody, signing, transaction, settlement, canonical disposition, release, publication, or deployment authority.
