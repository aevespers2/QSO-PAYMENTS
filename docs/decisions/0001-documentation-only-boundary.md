# ADR-0001: Documentation-only first release

- **Status:** Proposed; requires charter approval
- **Date:** 2026-07-19
- **Decision owners:** Repository architect and designated human reviewers
- **Applies to:** QSO-PAYMENTS initial release line

## Context

Payment terminology can imply custody, transfer authority, regulated activity, legal suitability, finality, or investment expectations even when a repository contains only concepts or interfaces. The project needs a shared vocabulary and explicit trust boundaries before schemas, accounting engines, adapters, testnet integration, or production claims can be evaluated safely.

The repository already describes payment intent, allocations, receipts, disputes, distribution patterns, and adapter boundaries. Without an approved environment model, those descriptions could be mistaken for executable or authorized capabilities.

## Decision

The first QSO-PAYMENTS release will be **documentation only**. It may publish:

- project purpose, users, terminology, and ecosystem role;
- authority and trust boundaries;
- environment labels and prohibited implications;
- proposed record families and invariants;
- threat, privacy, accessibility, publication, provenance, and rollback guidance;
- fictional examples that contain no credentials or real financial data.

It will not publish or activate:

- executable payment schemas represented as stable contracts;
- accounting or reconciliation engines;
- custody, key management, signing, or transaction broadcasting;
- credentialed adapters;
- testnet or production integration;
- investment products, yield or return promises;
- legal or compliance certification.

## Rationale

This sequence makes the authority model reviewable before code can harden ambiguous assumptions. It also creates a public record of what the repository does not do, reduces environment confusion, and provides acceptance gates for later simulation-only work.

## Consequences

### Positive

- Readers can distinguish proposal, validation, authorization, allocation, submission, receipt, reconciliation, and dispute.
- Claims can be reviewed against one explicit environment model.
- Later schemas and fixtures have documented invariants and failure semantics.
- Publication, accessibility, privacy, security, provenance, and rollback become first-class release concerns.

### Costs

- No executable payment demonstration is included in the first release.
- Schema and adapter decisions remain blocked until the charter is approved.
- Documentation requires independent claims, security, privacy, accessibility, and release review.
- Some terminology and jurisdictional assumptions may change after specialist review.

## Alternatives considered

### Publish schemas immediately

Rejected for the first release because a schema can appear authoritative even when terminology, approval semantics, privacy, compatibility, and jurisdictional assumptions are unresolved.

### Add a simulation engine first

Rejected because executable behavior would embed arithmetic, replay, failure, and state-transition decisions before the governing contract is approved.

### Provide disabled adapter implementations

Rejected because code containing authentication or transaction-shaping behavior can create capability, supply-chain, secret-handling, and user-expectation risks even when disabled.

### Avoid payment documentation entirely

Rejected because the QSO ecosystem still needs a precise boundary for economic proposals and evidence. A carefully constrained documentation product provides value without activating financial authority.

## Approval criteria

This ADR may become accepted only when the charter approves intended users, terminology, jurisdictional assumptions, privacy model, license, ecosystem role, environment labels, prohibited capabilities, and review ownership. Acceptance of this ADR does not authorize simulation, testnet, or production work; each requires a separate decision and release plan.

## Follow-up decisions

- Canonical record and schema identifiers
- Fixed-precision arithmetic and rounding policy
- Authorization identity and revocation model
- Canonicalization, hashing, and signature boundaries
- Retention and privacy model
- Simulation fixture format
- Adapter interface and environment governance
- Compatibility and migration policy
