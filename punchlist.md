# Documentation Release Punch List

This checklist records evidence for the documentation-only candidate. A checked item requires a durable link to the exact commit, workflow run, report, artifact, checksum, review, or approval. Creating or editing this file does not satisfy a gate.

## P0 — Charter and portfolio authority approval

- [ ] Intended users and supported use cases approved
- [ ] Canonical terminology and status vocabulary approved
- [ ] Jurisdictional, regulatory, tax, and licensing assumptions approved or explicitly deferred with limits
- [ ] QSO-PAYMENTS role as A.L.I.S.T.A.I.R.E.'s bounded economic-intent, evidence, dispute, and reconciliation subsystem approved
- [ ] Repository `0` resource-proposal role approved
- [ ] Repository `1` generic capability/canonical-state role approved or replaced
- [ ] Independent financial authorizer and revoker designated
- [ ] Adapter credential, signing, custody, monitoring, and incident owners designated
- [ ] Portfolio-wide emergency-stop, correction, revocation, recovery, and rollback owners designated
- [ ] Shared schema/package and identity-namespace owner approved
- [ ] Data classification, privacy, retention, disclosure, and deletion model approved
- [ ] Documentation, simulation, testnet, and production labels and transitions approved
- [ ] Prohibited capabilities, self-authorization rules, and claims approved
- [ ] Architecture, security, privacy, accessibility, claims/legal, and release reviewers named

Evidence: _pending_

## P1 — Obstruction and gluing approval

- [ ] Financial approval is distinct from generic capability issuance
- [ ] Resource proposal is distinct from validated payment intent
- [ ] Financial authorization is distinct from an execution credential
- [ ] Adapter execution is distinct from receipt validation, reconciliation, canonical acceptance, and legal finality
- [ ] Repository `0` → QSO-PAYMENTS → review → financial authority → Repository `1` route approved
- [ ] Intent, authorization, capability, receipt, dispute, reconciliation, correction, and revocation schema ownership approved
- [ ] Requester, beneficiary, payee, destination, device, environment, and adapter identity namespaces approved
- [ ] Environment transition state machine approved
- [ ] Currency, unit, fixed precision, rounding, fee, tax, and remainder semantics approved
- [ ] Quote source, valuation time, freshness, and exchange-rate rules approved
- [ ] Shared idempotency, nonce, retry, replay, and duplicate domains approved
- [ ] Finality, pending, failure, unknown, dispute, reversal, and reconciliation semantics approved
- [ ] Correction, supersession, cache invalidation, and downstream notification rules approved
- [ ] All eight pairwise contract edges reviewed
- [ ] All six triple-overlap witness groups approved
- [ ] The 18 active obstructions are resolved, explicitly deferred, or accepted with bounded risk

Evidence: _pending_

## P2 — Machine-readable compatibility evidence

- [ ] Canonical schemas are published from the approved owner repository
- [ ] Every schema has an immutable version and compatibility policy
- [ ] Canonical serialization and signature scope are defined
- [ ] Identical positive fixtures pass in all participating repositories
- [ ] Malformed, unsupported-version, stale, replayed, wrong-identity, and expected-head mismatch fixtures fail closed
- [ ] Over-limit, wrong-destination, wrong-environment, expired, and revoked authorization fixtures fail closed
- [ ] Idempotency and duplicate-suppression fixtures prevent repeated effects
- [ ] Fixed-precision allocation and reconciliation golden vectors pass
- [ ] Quote freshness and exchange-rate evidence fixtures pass
- [ ] Partial failure, timeout, retry, reversal, refund, dispute, and compensation fixtures pass
- [ ] Adapter evidence preserves raw hashes, redaction declarations, uncertainty, and correction routes
- [ ] Revocation and emergency-stop propagation invalidates downstream use
- [ ] Recovery restores a bounded state without deleting incident evidence

Evidence: _pending; executable schemas and fixtures require separate approval_

## P3 — Source and build integrity

- [ ] Candidate commit is immutable and recorded
- [ ] Pull-request workflow asserted the submitted head SHA
- [ ] Clean checkout reproduced
- [ ] `python -m pip install -r requirements-docs.txt` passed
- [ ] `mkdocs build --strict` passed
- [ ] Required files and local links validated
- [ ] Workflow permissions reviewed
- [ ] Action and dependency versions recorded
- [ ] Source archive retained
- [ ] Generated Pages artifact retained
- [ ] Source-identity record retained
- [ ] SHA-256 manifest retained
- [ ] Provenance record retained
- [ ] Generated output contains no credentials, account data, or deployment secrets

Evidence: _pending accepted exact-head result after the current documentation changes_

## Content and claims

- [ ] Purpose and non-goals are consistent across README, Pages, task chain, punch list, release plan, and changelog
- [ ] A.L.I.S.T.A.I.R.E. objective and QSO-PAYMENTS subsystem role are consistent
- [ ] Repository `0`, Repository `1`, financial authorization, and adapter roles are distinct
- [ ] Intent, validation, authorization, capability, allocation, adapter submission, receipt, reconciliation, dispute, custody, and settlement are distinct
- [ ] Every capability claim has an environment label
- [ ] No custody, signing, settlement-service, investment, certification, suitability, or return promise is implied
- [ ] No QSO, genome, repository, task, interface, successful workflow, or transported record is represented as financial authority
- [ ] Finality, pending, unknown, reversal, and dispute limitations are visible
- [ ] Repository dependency descriptions do not transfer authority
- [ ] Architecture and gluing documents received human review

Evidence: _pending_

## Accessibility and usability

- [ ] Keyboard navigation and visible focus reviewed
- [ ] Heading structure and landmarks reviewed
- [ ] Link text and navigation reviewed
- [ ] Tables and code blocks reflow or scroll without loss
- [ ] Contrast reviewed
- [ ] 200% and 400% zoom reviewed
- [ ] Reduced-motion preference respected
- [ ] Warnings, authority states, environments, and result states do not rely on color alone
- [ ] Authority and environment distinctions are understandable without diagrams alone

Evidence: _pending_

## Security, privacy, and financial safety

- [ ] Source and build output scanned for secrets
- [ ] Source and build output inspected for personal or financial data
- [ ] External links and remote content reviewed
- [ ] Workflow and supply-chain risks reviewed
- [ ] Pull-request jobs have no Pages deployment or token-minting authority
- [ ] Self-approval and cross-repository authority-confusion threats reviewed
- [ ] Generic capability versus financial approval confusion reviewed
- [ ] Adapter substitution, replay, duplicate effect, receipt forgery, and false finality threats reviewed
- [ ] Credential, signing, custody, key rotation, and revocation topology independently reviewed
- [ ] Data minimization, tokenization, redaction, retention, and publication rules reviewed
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
- [ ] Financial-route emergency-stop and recovery tabletop completed before any executable environment
- [ ] Recovery evidence retained
- [ ] Unresolved findings recorded

Evidence: _pending_

## Approval

- [ ] Documentation reviewer approved
- [ ] Architecture reviewer approved
- [ ] Contract/gluing reviewer approved
- [ ] Security and privacy reviewers approved
- [ ] Accessibility reviewer approved
- [ ] Claims/legal reviewer approved where required
- [ ] Financial authority owner approved the separation-of-duties model
- [ ] A.L.I.S.T.A.I.R.E. portfolio authority approved subsystem placement
- [ ] Release owner approved publication

Decision: `BLOCKED`

Reason: Charter, financial-authority, schema ownership, compatibility witnesses, exact-head review evidence, publication approval, and recovery ownership remain pending. No simulation, testnet, adapter, or production work is authorized.
