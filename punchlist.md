# Documentation Release Punch List

This checklist records evidence for the documentation-only candidate. A checked item requires a durable link to the exact commit, workflow run, report, artifact, checksum, review, or approval. Creating or editing this file does not satisfy a gate.

## P0 — Charter and portfolio authority approval

- [ ] Intended users and supported use cases approved
- [ ] Canonical terminology and status vocabulary approved
- [ ] Jurisdictional, regulatory, tax, and licensing assumptions approved or explicitly deferred with limits
- [ ] QSO-PAYMENTS role as A.L.I.S.T.A.I.R.E.'s bounded economic-intent, evidence, dispute, and reconciliation subsystem approved
- [ ] Repository `0` resource-proposal and portable-host observation role approved
- [ ] Repository `1` device-enrollment, generic capability, and canonical-state role approved or replaced
- [ ] Device identity, ownership scope, enrollment generation, replacement, retirement, and revocation owner designated
- [ ] Workspace, repository, base-commit, and expected-head identity method approved
- [ ] Independent financial authorizer and revoker designated
- [ ] Adapter credential, signing, custody, monitoring, and incident owners designated
- [ ] Device stop, financial stop, adapter stop, portfolio freeze, recovery, and rollback owners designated
- [ ] Shared schema/package, status/reason-code, and identity-namespace owner approved
- [ ] Data classification, privacy, retention, disclosure, and deletion model approved
- [ ] Documentation, simulation, testnet, and production labels and transitions approved
- [ ] Prohibited capabilities, self-authorization rules, and claims approved
- [ ] Architecture, security, privacy, accessibility, claims/legal, and release reviewers named

Evidence: _pending_

## P1 — Obstruction and gluing approval

- [ ] Device enrollment is distinct from financial approval
- [ ] Device trust is distinct from workspace/repository authority
- [ ] Financial approval is distinct from generic capability issuance
- [ ] Resource proposal is distinct from validated payment intent
- [ ] Financial authorization is distinct from an execution credential
- [ ] Adapter execution is distinct from receipt validation, reconciliation, canonical acceptance, and legal finality
- [ ] Repository `0` → QSO-PAYMENTS → review → financial authority → Repository `1` route approved
- [ ] Device/workspace binding policy is approved for every execution-capable environment
- [ ] Wrong-device, wrong-enrollment-generation, wrong-workspace, wrong-head, wrong-adapter, and wrong-environment use fails closed
- [ ] Lost, stolen, revoked, retired, and replacement-device lifecycle approved
- [ ] Intent, authorization, capability, receipt, dispute, reconciliation, correction, revocation, device, workspace, status, reason-code, and recovery schema ownership approved
- [ ] Requester, beneficiary, payee, destination, device, environment, workspace, and adapter identity namespaces approved
- [ ] Environment transition state machine approved
- [ ] Currency, unit, fixed precision, rounding, fee, tax, and remainder semantics approved
- [ ] Quote source, valuation time, freshness, and exchange-rate rules approved
- [ ] Shared idempotency, nonce, retry, replay, and duplicate domains approved
- [ ] Finality, pending, failure, unknown, dispute, reversal, and reconciliation semantics approved
- [ ] Correction, supersession, cache invalidation, and downstream notification rules approved
- [ ] Three independent stop domains—device, financial, and adapter—approved
- [ ] All pairwise contract edges reviewed
- [ ] All triple-overlap witness groups approved
- [ ] Active obstructions are resolved, explicitly deferred, or accepted with bounded risk

Evidence: _pending_

## P1A — Conceptual contract and interface review

- [ ] Interface surfaces identify producer, consumer, boundary, and current disposition
- [ ] Common envelope semantics distinguish profile, record, context, provenance, classification, and payload
- [ ] Proposal, intent, validation, financial authorization, allocation, capability, adapter submission, adapter evidence, reconciliation, and dispute records remain distinct
- [ ] Status labels have one explicit meaning and one or more prohibited interpretations
- [ ] Unknown statuses and reason codes fail closed
- [ ] Examples are visibly synthetic and non-executable
- [ ] Compatibility and migration requirements preserve source lineage, unsupported fields, consumer closure, and rollback
- [ ] Contract reference is reviewed without being represented as an approved schema or API

Evidence: _pending_

## P2 — Machine-readable compatibility evidence

- [ ] Canonical schemas are published from the approved owner repository
- [ ] Every schema has an immutable version and compatibility policy
- [ ] Canonical serialization and signature scope are defined
- [ ] Status and reason-code registries are closed, versioned, and independently reviewed
- [ ] Identical positive fixtures pass in all participating repositories
- [ ] Malformed, unsupported-version, stale, replayed, wrong-identity, and expected-head mismatch fixtures fail closed
- [ ] Wrong-device, revoked-device, stale-enrollment, wrong-workspace, and replacement-device fixtures fail closed
- [ ] Over-limit, wrong-destination, wrong-environment, expired, and revoked authorization fixtures fail closed
- [ ] Idempotency and duplicate-suppression fixtures prevent repeated effects
- [ ] Fixed-precision allocation and reconciliation golden vectors pass
- [ ] Quote freshness and exchange-rate evidence fixtures pass
- [ ] Partial failure, timeout, retry, reversal, refund, dispute, and compensation fixtures pass
- [ ] Adapter evidence preserves raw hashes, redaction declarations, uncertainty, device identity, workspace identity, and correction routes
- [ ] Device, financial, and adapter revocation propagation invalidates downstream use and cached review state
- [ ] Lost-device and replacement-device fixtures preserve evidence and require fresh admissible bindings
- [ ] Recovery restores a bounded state without deleting incident evidence

Evidence: _pending; executable schemas and fixtures require separate approval_

## P3 — Source and build integrity

- [ ] Candidate commit is immutable and recorded
- [ ] Pull-request workflow asserted the submitted head SHA
- [ ] Clean checkout reproduced
- [ ] `python -m pip install -r requirements-docs.txt` passed
- [ ] `mkdocs build --strict` passed
- [ ] Required files and local links validated
- [ ] Contract and accessibility guides appear in rendered navigation
- [ ] Workflow permissions reviewed
- [ ] Action and dependency versions recorded
- [ ] Source archive retained
- [ ] Generated Pages artifact retained
- [ ] Source-identity record retained
- [ ] SHA-256 manifest retained
- [ ] Provenance record retained
- [ ] Generated output contains no credentials, account data, device identifiers, network inventories, authorization records, or deployment secrets

Evidence: _pending accepted exact-head result after the current documentation changes_

## Content and claims

- [ ] Purpose and non-goals are consistent across README, Pages, task chain, punch list, release plan, and changelog
- [ ] A.L.I.S.T.A.I.R.E. objective and QSO-PAYMENTS subsystem role are consistent
- [ ] Repository `0`, Repository `1`, financial authorization, device trust, workspace identity, and adapter roles are distinct
- [ ] Intent, validation, authorization, capability, allocation, adapter submission, receipt, reconciliation, dispute, custody, and settlement are distinct
- [ ] Device enrollment is never described as financial permission
- [ ] Financial authorization is never described as general device or repository authority
- [ ] Every capability claim has an environment, device, and workspace binding or explicitly states that no executable capability exists
- [ ] No custody, signing, settlement-service, investment, certification, suitability, or return promise is implied
- [ ] No QSO, genome, repository, task, interface, trusted device, successful workflow, or transported record is represented as financial authority
- [ ] Finality, pending, unknown, reversal, and dispute limitations are visible
- [ ] Status and reason-code examples do not imply executable contract acceptance
- [ ] Repository dependency descriptions do not transfer authority
- [ ] Architecture, contract-reference, accessibility, and gluing documents received human review

Evidence: _pending_

## Accessibility and usability

- [ ] Keyboard navigation and visible focus reviewed
- [ ] Heading structure and landmarks reviewed
- [ ] Link text and navigation reviewed
- [ ] Tables and code blocks reflow or scroll without loss
- [ ] Contrast reviewed
- [ ] 200% and 400% zoom reviewed
- [ ] Reduced-motion preference respected
- [ ] Warnings, authority states, environments, device states, and result states do not rely on color alone
- [ ] Authority, device, workspace, environment, and finality distinctions are understandable without diagrams alone
- [ ] Every meaningful diagram has equivalent prose
- [ ] Every example is labeled illustrative, synthetic, or executable
- [ ] A reader unfamiliar with the portfolio can identify proposer, validator, authorizer, capability issuer, adapter, reconciler, correction/revocation owner, and unresolved state

Evidence: _pending_

## Security, privacy, and financial safety

- [ ] Source and build output scanned for secrets
- [ ] Source and build output inspected for personal, device, network, or financial data
- [ ] External links and remote content reviewed
- [ ] Workflow and supply-chain risks reviewed
- [ ] Pull-request jobs have no Pages deployment or token-minting authority
- [ ] Self-approval and cross-repository authority-confusion threats reviewed
- [ ] Device-trust versus financial-approval confusion reviewed
- [ ] Workspace/repository authority versus device ownership confusion reviewed
- [ ] Generic capability versus financial approval confusion reviewed
- [ ] Wrong-device, stale-enrollment, lost-device, replacement-device, and cached-approval threats reviewed
- [ ] Adapter substitution, replay, duplicate effect, receipt forgery, and false finality threats reviewed
- [ ] Credential, signing, custody, key rotation, device binding, and revocation topology independently reviewed
- [ ] Host evidence and financial evidence remain separately minimized and governed
- [ ] Data minimization, tokenization, redaction, retention, and publication rules reviewed
- [ ] Public examples contain no credentials, complete account identifiers, private device identifiers, or production transaction references
- [ ] Automated budget-escalation and self-funding loops reviewed
- [ ] Incident contacts, containment authority, independent emergency disable, and recovery order recorded

Evidence: _pending_

## Deployment and recovery

- [ ] Pages publication is separately authorized
- [ ] Deployment from the exact candidate commit succeeded
- [ ] Published URL and deployed commit verified
- [ ] Post-deployment navigation and claims check passed
- [ ] Prior verified artifact identified
- [ ] Documentation rollback procedure exercised or credibly demonstrated
- [ ] Correction or withdrawal updates every controlled documentation route
- [ ] Device loss/theft, financial revocation, adapter disable, and replacement-device tabletop completed before any executable environment
- [ ] Financial-route emergency-stop and recovery tabletop completed before any executable environment
- [ ] Recovery evidence retained
- [ ] Unresolved findings recorded

Evidence: _pending_

## Approval

- [ ] Documentation reviewer approved
- [ ] Architecture reviewer approved
- [ ] Contract/gluing reviewer approved
- [ ] Contract-reference reviewer approved the conceptual semantics without treating them as an executable API
- [ ] Portable device-trust reviewer approved
- [ ] Security and privacy reviewers approved
- [ ] Accessibility reviewer approved the rendered artifact
- [ ] Claims/legal reviewer approved where required
- [ ] Financial authority owner approved the separation-of-duties model
- [ ] Device-enrollment authority approved device/workspace bindings and replacement behavior
- [ ] A.L.I.S.T.A.I.R.E. portfolio authority approved subsystem placement
- [ ] Release owner approved publication

Decision: `BLOCKED`

Reason: Charter, financial-authority, device/workspace identity, schema/status/reason-code ownership, compatibility witnesses, exact-head review evidence, rendered accessibility review, publication approval, and recovery ownership remain pending. No simulation, testnet, adapter, device-control, or production payment work is authorized.
