# Documentation Release Punch List

This checklist records evidence for the documentation-only candidate. A checked item requires a durable link to the exact commit, workflow run, report, artifact, checksum, review, or approval. Creating this file does not satisfy any gate.

## P0 — Charter and portfolio authority approval

- [ ] Intended users approved
- [ ] Canonical terminology approved
- [ ] Jurisdictional and regulatory assumptions approved or explicitly deferred with limits
- [ ] QSO-PAYMENTS role as A.L.I.S.T.A.I.R.E.'s bounded economic-intent and evidence subsystem approved
- [ ] Canonical autonomous-development control plane designated
- [ ] Independent financial capability issuer and revoker designated
- [ ] Adapter credential, signing, custody, monitoring, and incident owners designated
- [ ] Portfolio-wide emergency-stop and rollback authority designated
- [ ] Cross-repository exchange and schema ownership approved
- [ ] Data classification, privacy, retention, and disclosure model approved
- [ ] License and public-documentation rights approved
- [ ] Documentation, simulation, testnet, and production labels approved
- [ ] Prohibited capabilities, self-authorization rules, and claims approved
- [ ] Architecture, security, privacy, accessibility, claims, and release review owners named

Evidence: _pending_

## P1 — Source and build integrity

- [ ] Candidate commit is immutable and recorded
- [ ] Pull-request workflow asserted the submitted head SHA
- [ ] Clean checkout reproduced
- [ ] `python -m pip install -r requirements-docs.txt` passed
- [ ] `mkdocs build --strict` passed
- [ ] Workflow permissions reviewed
- [ ] Action and dependency versions recorded
- [ ] Source archive retained
- [ ] Generated Pages artifact retained
- [ ] Source-identity record retained
- [ ] SHA-256 manifest retained
- [ ] Provenance record retained

Evidence: _pending accepted exact-head workflow result_

## Content and claims

- [ ] Purpose and non-goals are consistent across README, Pages, task chain, release plan, and changelog
- [ ] A.L.I.S.T.A.I.R.E. system objective and QSO-PAYMENTS subsystem role are consistent
- [ ] Autonomous-development orchestration and financial authorization remain separate
- [ ] Intent, validation, authorization, allocation, adapter submission, receipt, reconciliation, and dispute are distinct
- [ ] Every capability claim has an environment label
- [ ] No custody, signing, settlement-service, investment, certification, suitability, or return promise is implied
- [ ] No QSO, genome, repository, task, or control-plane identity is represented as financial authority
- [ ] Finality and unresolved-state limitations are visible
- [ ] Repository dependency descriptions do not transfer authority
- [ ] Architecture and design documents received human review

Evidence: _pending_

## Accessibility and usability

- [ ] Keyboard navigation and visible focus reviewed
- [ ] Heading structure and landmarks reviewed
- [ ] Link text and navigation reviewed
- [ ] Tables and code blocks reflow or scroll without loss
- [ ] Contrast reviewed
- [ ] 200% and 400% zoom reviewed
- [ ] Reduced-motion preference respected
- [ ] Warnings and environment states do not rely on color alone
- [ ] Authority and environment distinctions are understandable without diagrams alone

Evidence: _pending_

## Security and privacy

- [ ] Source and build output scanned for secrets
- [ ] Source and build output inspected for personal financial data
- [ ] External links and remote content reviewed
- [ ] Workflow and supply-chain risks reviewed
- [ ] Pull-request jobs have no Pages deployment or token-minting authority
- [ ] Self-approval and cross-repository authority-confusion threats reviewed
- [ ] Claim and environment-confusion threats reviewed
- [ ] Data minimization and publication rules reviewed
- [ ] Incident contacts, containment authority, and independent emergency disable recorded

Evidence: _pending_

## Deployment and recovery

- [ ] Pages deployment from exact candidate commit succeeded
- [ ] Published URL and deployed commit verified
- [ ] Post-deployment navigation and claims check passed
- [ ] Prior verified artifact identified
- [ ] Rollback procedure exercised or credibly demonstrated
- [ ] Recovery evidence retained
- [ ] Unresolved findings recorded

Evidence: _pending_

## Approval

- [ ] Documentation reviewer approved
- [ ] Architecture reviewer approved
- [ ] Security/privacy reviewers approved
- [ ] Accessibility reviewer approved
- [ ] Claims/legal reviewer approved where required
- [ ] A.L.I.S.T.A.I.R.E. portfolio authority owner approved subsystem placement
- [ ] Release owner approved publication

Decision: `BLOCKED`

Reason: P0 charter and portfolio authority decisions plus all retained publication evidence are pending.
