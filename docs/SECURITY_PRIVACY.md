# Security and privacy

QSO-PAYMENTS treats payment language, authorization records, financial metadata, adapter configuration, and publication claims as elevated-risk material. The current documentation-only boundary reduces exposure but does not remove the need for threat modeling and data minimization.

## Trust boundaries

```text
Untrusted proposal
    |
    v
Schema and policy evaluation
    |
    v
Independent authorization boundary
    |
    v
Deterministic allocation and reconciliation
    |
    v
Disabled adapter gate
    |
    +----> documentation or simulation evidence
    |
    `----> separately approved external system [not currently authorized]
```

No identity, repository membership, QSO genome, prior approval, model output, or successful validation crosses the authorization boundary automatically.

## Threat inventory

| Threat | Required response |
|---|---|
| Forged authorization | Bind approval to an authenticated subject, exact intent digest, scope, expiry, and revocation state |
| Replay or duplicate submission | Use idempotency keys, bounded retries, duplicate detection, and reconciliation before retry |
| Environment confusion | Put an explicit environment on every record, example, page, and adapter configuration |
| Allocation manipulation | Use deterministic fixed-precision arithmetic and fail on unreconciled totals |
| Adapter substitution | Bind adapter identity, version, environment, request digest, and response evidence |
| Receipt forgery or overclaim | Verify source where possible and preserve finality limitations and unknown states |
| Credential leakage | Keep secrets out of source, fixtures, logs, artifacts, screenshots, and public evidence |
| Privacy leakage | Minimize identifiers, redact evidence, separate public and restricted records, define retention |
| Workflow compromise | Use least permissions, pinned dependencies, clean builds, provenance, checksums, and review |
| Misleading financial claims | Classify claims and prohibit custody, settlement, certification, suitability, or return promises |

## Data-classification model

### Public documentation

Architecture descriptions, fictional fixtures, diagrams, terminology, and review procedures may be public after claims, privacy, security, and accessibility review.

### Internal operational data

Workflow logs, incident records, unpublished review findings, adapter configuration, and rollback evidence require access control and a documented retention policy.

### Sensitive financial metadata

Amounts tied to identifiable people, counterparties, account references, transaction references, dispute evidence, and routing metadata are minimized, encrypted where stored, redacted before publication, and accessed only for an approved purpose.

### Secrets

Private keys, API credentials, signing material, recovery phrases, access tokens, and authentication cookies are prohibited in repository content, fixtures, documentation builds, and generated evidence. A detected secret requires immediate containment and rotation; deleting the file alone is insufficient.

## Privacy principles

1. Collect only fields required for a declared purpose.
2. Prefer pseudonymous identifiers and separate identity resolution from payment records.
3. Do not place personal financial data in URLs, branch names, issue titles, examples, screenshots, or public build artifacts.
4. Define retention and deletion obligations before any non-fictional data is accepted.
5. Preserve audit evidence without publishing unnecessary personal information.
6. Treat disputes and failures as potentially more sensitive than successful outcomes.
7. Record access and disclosure decisions for restricted evidence.

## Claims controls

Public documentation must not imply that QSO-PAYMENTS:

- holds or safeguards assets;
- signs or broadcasts transactions;
- provides banking, brokerage, escrow, money-transmission, or investment services;
- guarantees settlement, finality, reversibility, identity, compliance, or returns;
- is approved for a jurisdiction or regulated activity;
- has a testnet or production adapter merely because an interface is described.

Use evidence-qualified language such as “proposed,” “documentation-only,” “simulation candidate,” “adapter-reported,” “unresolved,” and “separately approved.”

## Workflow and supply-chain controls

The documentation workflow should:

- use least-privilege GitHub permissions;
- disable persisted checkout credentials;
- pin the documentation tool version;
- fail on MkDocs warnings;
- retain the exact commit and dependency versions;
- scan repository and build output for secrets and unexpected files;
- record artifact hashes and workflow provenance;
- avoid unreviewed remote scripts in the public site;
- require human release approval after technical checks.

A successful build proves only that the site compiled. It does not prove claim accuracy, accessibility, privacy, security, legal suitability, or release readiness.

## Incident triggers

Initiate incident handling when:

- a secret or sensitive record appears in source, history, logs, or published output;
- a page implies unauthorized custody, settlement, production readiness, or guaranteed returns;
- a workflow gains unnecessary permissions or executes unexpected code;
- a documentation artifact differs from its recorded checksum;
- a dependency or action is compromised;
- a published diagram or example exposes real account or identity data;
- rollback cannot restore the last verified artifact.

Follow [Operations and recovery](OPERATIONS.md), preserve evidence, and avoid publishing additional sensitive details while investigating.
