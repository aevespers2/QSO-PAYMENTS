# Obstruction and Gluing Analysis

## Purpose

This document analyzes whether QSO-PAYMENTS can compose safely with the current A.L.I.S.T.A.I.R.E. repository portfolio without silently transferring financial authority, identity, canonical-state ownership, or settlement claims between repositories.

The language of **obstructions**, **local sections**, and **gluing witnesses** is used as an engineering discipline. It does not claim a completed mathematical cohomology calculation. A local repository description is considered glueable only when the overlapping contracts agree and deterministic evidence demonstrates the agreement.

> **Current release surface:** documentation only. No schema, adapter, credential, custody, signature, testnet route, production transfer, publication, or financial capability is activated by this analysis.

## Candidate ownership model

The lowest-coupling portfolio split is:

| Concern | Candidate owner | Boundary |
|---|---|---|
| Product mission and portfolio governance | `ALISTAIRE-` | Defines accepted architecture and governance; does not approve individual payments |
| Resource discovery and engineering proposal | Repository `0` | May prepare a bounded resource proposal; cannot approve or fund it |
| Portable canonical state and generic capability control | Repository `1` | May validate and record a narrowly scoped execution capability after required financial approval; does not create financial approval by itself |
| Economic intent, allocation preview, evidence, dispute, and reconciliation semantics | `QSO-PAYMENTS` | Owns the payment-intent lifecycle and fail-closed interpretation; holds no credentials or custody |
| Human review surface | `QSO-STUDIO` or another approved interface | Displays evidence and captures attributable decisions; UI interaction alone is not authority |
| Declarative identity and policy references | `QSO-GENOMES` | Supplies versioned descriptive references; cannot grant financial authority |
| Collaboration and experiment budgets | `QSO-FABRIC` | May consume approved limits or produce proposals; cannot approve or settle them |
| Exchange and interpretation profiles | `QSO-DIGITALIS` | Defines inert profile-specific projections where approved; does not authorize execution |
| Transport or independent evidence profile | `Bridge` or an extracted approved profile | Carries or verifies bounded evidence; transport success is not settlement finality |
| Financial approval | Named human or separately approved financial authority | Approves exact economic scope, amount, destination class, environment, conditions, and expiry |
| External payment adapter | Separately governed service, currently disabled | Holds isolated credentials and executes only an accepted, unexpired capability |

This is a documentation candidate. Repository names do not establish authority by themselves.

## Primary material obstruction

The portfolio has not yet separated **financial approval** from **generic capability issuance** in one jointly versioned contract.

Repository `1` is documented as a candidate capability and canonical-state authority. QSO-PAYMENTS is documented as the economic-intent and evidence subsystem. A financial approver may be a human or separately approved service. Unless those roles are glued explicitly, any of the following unsafe interpretations is possible:

1. a Repository `0` proposal is treated as approved because it entered QSO-PAYMENTS;
2. a generic Repository `1` capability is treated as financial approval;
3. a human approval displayed in QSO-STUDIO is treated as an executable credential;
4. adapter execution is treated as canonical settlement merely because a command succeeded;
5. a QSO genome, policy reference, or prior approval is treated as reusable financial authority.

The lowest-coupling repair candidate is:

```text
Repository 0 local proposal
→ QSO-PAYMENTS validated economic intent
→ review packet
→ independent financial authorization record
→ Repository 1 admission and narrowly scoped execution capability
→ disabled external adapter boundary
→ execution evidence
→ QSO-PAYMENTS reconciliation
→ Repository 1 canonical disposition
```

Every arrow requires a versioned record, explicit identity, expected state, expiry, revocation behavior, and negative fixtures. No stage inherits the authority of another stage.

## Active obstruction ledger

| ID | Obstruction | Consequence if unresolved | Required witness |
|---|---|---|---|
| PAY-O01 | Financial approval and generic capability issuance are not formally separated | A technical capability may be misrepresented as permission to spend | Distinct authorization and capability schemas plus rejection fixtures |
| PAY-O02 | Repository `0` proposal identity and payment-intent identity are not jointly versioned | Duplicate, stale, or wrong-task requests may be funded | Proposal-to-intent mapping fixture with immutable objective and task references |
| PAY-O03 | Requester, beneficiary, payee, destination, device, environment, and adapter identities lack one namespace policy | Records may refer to the wrong person, account, device, or environment | Namespace registry and wrong-identity negative fixtures |
| PAY-O04 | Canonical ownership of intent, authorization, capability, receipt, dispute, and reconciliation envelopes is unresolved | Competing schemas may diverge silently | One package owner, compatibility matrix, and migration tests |
| PAY-O05 | Documentation, simulation, testnet, and production transitions lack a shared state machine | A harmless simulation record may be routed toward a real adapter | Environment transition table with fail-closed downgrade and escalation tests |
| PAY-O06 | Currency, unit, fixed precision, rounding, remainder, fee, and tax semantics are not portfolio-wide | Totals may not reconcile or may produce hidden exposure | Golden allocation vectors and invariant tests |
| PAY-O07 | Quote source, exchange rate, valuation time, freshness, and market-closure semantics are undefined | Stale or unverifiable values may be treated as current cost | Versioned quote evidence and stale-source rejection fixtures |
| PAY-O08 | Idempotency, retry, replay, nonce, and duplicate domains are not shared across proposal, capability, and adapter records | Retries may duplicate financial effects | End-to-end replay and partial-retry fixtures |
| PAY-O09 | Destination and account data minimization, tokenization, redaction, retention, and disclosure ownership are unresolved | Sensitive financial data may leak into repositories, logs, models, or Pages artifacts | Data-classification profile and redaction tests |
| PAY-O10 | Credential, private-key, signing, custody, rotation, and revocation topology is undefined | A repository or model process may inherit secrets or irreversible authority | Offline key-custody design and independent revocation drill |
| PAY-O11 | Adapter receipt, network acceptance, processor status, ledger posting, legal finality, and reconciliation are conflated | A provisional response may be reported as settled | Multi-stage finality model and `UNKNOWN`/pending fixtures |
| PAY-O12 | Partial failure, timeout, refund, reversal, chargeback, dispute, escrow, and compensation semantics are incomplete | Funds or evidence may diverge without a safe recovery state | Failure matrix and deterministic compensation fixtures |
| PAY-O13 | QSO-PAYMENTS local evidence and Repository `1` canonical state are not reconciled atomically | Execution may succeed while canonical state remains stale, or vice versa | Expected-head, two-phase disposition, and recovery fixtures |
| PAY-O14 | Correction, supersession, revocation, cache invalidation, and downstream notification ownership is unresolved | Interfaces or autonomous planners may continue using revoked authority or stale receipts | Revocation propagation and stale-cache tests |
| PAY-O15 | QSO-STUDIO approval display, Bridge evidence transport, and QSO-DIGITALIS exchange profiles overlap without authority labels | A displayed, transported, or transformed record may be mistaken for approval | Authority-preserving transformation and UI confirmation fixtures |
| PAY-O16 | QSO-FABRIC budget coordination and QSO-PAYMENTS allocation responsibility overlap | Experiment orchestration may silently become purchasing authority | Fabric-to-payment proposal profile with explicit non-authority assertions |
| PAY-O17 | Automated budget feedback can create self-funding or escalating-resource loops | A system may repeatedly request more resources based on its own outputs | Per-objective caps, cooldowns, independent review, and loop-detection fixtures |
| PAY-O18 | Portfolio emergency stop, adapter disable, evidence preservation, recovery, and bounded restart are not jointly owned | A compromised or uncertain route may continue operating or lose evidence | Cross-repository freeze-and-recovery tabletop with immutable evidence |

## Pairwise gluing contracts

### Repository `0` → QSO-PAYMENTS

**Record:** resource proposal.

Required fields include immutable proposal ID, objective and task references, requester identity, purpose, requested unit and cap, environment, expiry, evidence references, alternatives, conflicts, policy reference, and idempotency key.

The receiver must reject missing provenance, self-approval claims, credentials, unsupported environment, stale proposals, replay, or an amount outside documented limits.

### QSO-PAYMENTS → QSO-STUDIO

**Record:** review packet.

The interface must preserve intent identity, evidence, uncertainty, amount and exposure, environment, retention class, requested authority, and unresolved conflicts. Display or button activation is not approval unless an approved identity and authorization protocol produce a separate attributable record.

### Financial authority → QSO-PAYMENTS

**Record:** financial authorization.

The authorization must identify the approver or approved service role, exact intent, amount limit, destination or destination class, permitted environment, conditions, timestamps, expiry, revocation path, jurisdictional assumptions, and policy version. It must be unusable for another intent or environment.

### QSO-PAYMENTS → Repository `1`

**Record:** capability-admission request.

Repository `1` verifies that the financial authorization is authentic, current, unrevoked, correctly scoped, and compatible with policy. If accepted, Repository `1` may issue a narrower execution capability. It must not broaden amount, destination, environment, duration, or adapter scope.

### Repository `1` → external adapter

**Record:** execution capability and adapter instruction.

The adapter accepts only its own identity, exact environment, permitted action, expected pre-state, limits, expiry, nonce, and policy version. Credentials stay outside repository and QSO records. The adapter returns evidence, not canonical acceptance.

### External adapter or Bridge profile → QSO-PAYMENTS

**Record:** execution evidence.

Evidence must preserve adapter identity, intent, capability, attempt, timestamps, status, processor references, redacted destination reference, amounts and fees, provisional/final status, raw-evidence hash, and correction route. Missing or contradictory evidence remains `UNKNOWN` or disputed.

### QSO-PAYMENTS → QSO-FABRIC

**Record:** approved budget status or reconciliation summary.

Fabric may consume bounded status for planning but cannot receive reusable credentials, broaden the approval, or infer authority for another experiment.

### QSO-PAYMENTS → Repository `1`

**Record:** reconciliation and canonical-disposition proposal.

Canonical disposition occurs only after evidence validation, expected-head checks, correction/revocation review, and independent policy evaluation. Adapter success alone does not force acceptance.

## Required triple-overlap witnesses

### 1. Repository `0` → QSO-PAYMENTS → QSO-STUDIO

Prove that a proposal becomes a reviewable intent without becoming approved. Fixtures must include valid, malformed, stale, replayed, over-limit, wrong-environment, missing-evidence, and self-approval cases.

### 2. QSO-STUDIO → financial authority → Repository `1`

Prove that an attributable human or approved-service decision becomes a narrowly scoped admission request and capability without the interface, QSO-PAYMENTS, or Repository `1` inventing financial approval.

### 3. QSO-PAYMENTS → Repository `1` → external adapter

Prove amount, destination class, environment, expiry, expected state, nonce, and revocation remain equal or narrower across all three records. Unsupported or broadened scope must fail closed.

### 4. External adapter → Bridge/evidence profile → QSO-PAYMENTS

Prove transformations preserve raw-evidence hashes, redaction declarations, status uncertainty, correction paths, and finality limits. Transport or verification success must not convert provisional evidence into settlement.

### 5. QSO-PAYMENTS → QSO-FABRIC → Repository `1`

Prove a budget or cost result can inform an experiment without becoming reusable financial authority or bypassing canonical policy. Duplicate requests from collaborative QSOs must remain deduplicated by the original intent and objective scope.

### 6. Revocation/emergency stop → adapter → reconciliation and recovery

Prove active capabilities are rejected after revocation, in-flight uncertainty is preserved, evidence remains immutable, downstream caches are invalidated, and restart requires an explicit bounded recovery decision.

## Shared result semantics

The portfolio should use explicit states rather than a single success boolean:

- `PROPOSED` — resource request exists; no approval;
- `VALIDATED` — structurally and policy-valid intent; no approval;
- `DENIED` — attributable decision refused the request;
- `EXPIRED` — applicable proposal, authorization, or capability is no longer current;
- `REVOKED` — authority was withdrawn;
- `HELD` — valid but intentionally not routed;
- `SIMULATED` — deterministic fictional result; no external effect;
- `SUBMITTED` — adapter accepted an instruction; finality unknown;
- `PENDING` — external process has not reached a terminal state;
- `FAILED` — bounded attempt failed with preserved evidence;
- `UNKNOWN` — evidence is incomplete, contradictory, or unverifiable;
- `DISPUTED` — an accepted record is challenged or requires adjudication;
- `REVERSED` — a previously reported effect was reversed;
- `RECONCILED` — evidence and expected accounting state agree under the accepted policy;
- `SUPERSEDED` — a correction replaced the record without deleting history.

Every status must identify the record to which it applies. A reconciled QSO-PAYMENTS record is not automatically a legal certification of settlement.

## Acceptance order

1. Approve QSO-PAYMENTS as the economic-intent and reconciliation owner, not a financial approver or custodian.
2. Name the independent financial approval authority and its human owners.
3. Approve Repository `1`'s role, if any, in admitting and revoking execution capabilities after financial approval.
4. Designate the canonical contract/package owner and identity namespaces.
5. Approve environment, amount, precision, quote, replay, privacy, retention, correction, and finality semantics.
6. Implement identical machine-readable schemas and fixtures in every participating repository.
7. Complete security, privacy, jurisdictional, accessibility, claims, incident, emergency-stop, and recovery review.
8. Reproduce exact-head documentation and fixture evidence before considering simulation.
9. Require separate explicit approval for testnet or production work.

## Architectural decisions still required

- Is Repository `1` the accepted capability and canonical-state authority for this route, or is a separate financial trust service required?
- Which human or approved service role may issue financial authorization, and who may revoke it?
- Which repository owns the shared intent, authorization, capability, receipt, dispute, and reconciliation schemas?
- Which identity and subject namespaces are canonical?
- Which jurisdictions, currencies, payment rails, privacy classes, retention periods, and licensing assumptions are in scope?
- Who owns credentials, signing, custody, adapter operation, monitoring, incident response, emergency stop, correction, and recovery?
- How are approval interfaces authenticated without placing secrets or sensitive data in public repositories?
- What evidence is required before documentation may advance to simulation, and before simulation may advance to any external environment?

Until these decisions and witnesses are accepted, QSO-PAYMENTS remains documentation-only with every external adapter disabled.
