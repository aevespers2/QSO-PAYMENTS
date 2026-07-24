# Documentation Release Punch List

This checklist governs the documentation-only candidate. A checked item requires a durable link to the exact commit, workflow run, rendered artifact, checksum, review, or approval. Editing this file, completing a template, or passing a build does not satisfy an authority or release gate.

## P0 — Charter and ownership

- [ ] Intended users, supported use cases, terminology, jurisdictions, privacy model, license, environment labels, and prohibited claims approved.
- [ ] QSO-PAYMENTS role as A.L.I.S.T.A.I.R.E.'s bounded economic-intent, allocation-preview, evidence, dispute, and reconciliation subsystem approved.
- [ ] Repository `0` proposal/observation role and Repository `1` device, capability, and canonical-disposition role approved or replaced.
- [ ] Device identity, ownership scope, enrollment generation, workspace/source identity, replacement, retirement, and revocation ownership designated.
- [ ] Independent financial authorizer and revoker designated with an approved authority-source model.
- [ ] Generic capability issuer/revoker, adapter credential/custody/signing owner, incident owner, emergency-stop owner, recovery owner, release owner, status-transition steward, and consumer-registration steward designated.
- [ ] Shared schema/package, status/reason-code, identity-namespace, compatibility, migration, and consumer-registration owner approved.
- [ ] Data classification, minimization, retention, disclosure, deletion, legal-hold, and correction model approved.
- [ ] Architecture, financial, contract, legal/finality, security, privacy, accessibility, claims, recovery, integration, and release reviewers named.

Evidence: _pending_

## P1 — Authority separation and gluing

- [ ] Resource proposal, validation, independent financial authorization, generic capability, adapter execution, receipt evidence, consumer projection, reconciliation, canonical disposition, custody, settlement, and legal finality remain distinct.
- [ ] Device enrollment is distinct from financial approval and workspace/repository authority.
- [ ] Financial authorization is distinct from a reusable credential or general technical capability.
- [ ] Adapter execution is distinct from receipt validation, consumer interpretation, reconciliation, canonical acceptance, and legal finality.
- [ ] Repository `0` → QSO-PAYMENTS → review → financial authority → Repository `1` route approved.
- [ ] Wrong requester, beneficiary, authorizer, destination, device, enrollment generation, workspace, repository, expected head, environment, adapter, amount, or time window fails closed.
- [ ] Lost, stolen, revoked, retired, and replacement-device lifecycle approved.
- [ ] Currency, unit, fixed precision, rounding, fee, tax, remainder, quote freshness, retry, replay, duplicate, partial-failure, unknown-outcome, dispute, reversal, correction, canonical-disposition, and legal-finality semantics approved.
- [ ] Device, financial, adapter, consumer, and portfolio stop domains and recovery order approved.
- [ ] Pairwise contract edges, triple-overlap witnesses, active obstructions, consumer reachability, and residual risks reviewed.

Evidence: _pending_

## P1A — Contract and interface reference

- [ ] Interface surfaces identify producer, consumer, boundary, and current disposition.
- [ ] Common envelope separates profile, record, context, provenance, classification, and payload.
- [ ] Proposal, intent, validation, financial authorization, allocation, capability, adapter submission, adapter evidence, reconciliation, dispute, correction, and revocation records remain distinct.
- [ ] Status labels have one explicit meaning and prohibited interpretations.
- [ ] Unknown profiles, statuses, fields, and reason codes fail closed.
- [ ] Examples are visibly synthetic and non-executable.
- [ ] Compatibility and migration preserve source lineage, unsupported fields, consumer closure, withdrawal, and rollback.
- [ ] The contract reference is reviewed without being represented as an approved schema or API.

Evidence: _pending_

## P1B — Independent financial-authorization review

- [ ] Review status remains `DOCUMENTED_NOT_AUTHORIZED` until a designated independent authority issues an exact decision.
- [ ] Authorizer identity, role, authority source, jurisdictional limits, and conflict-of-interest state are explicit.
- [ ] Exact intent identifier and digest are bound to the decision.
- [ ] Requester, beneficiary, payee, destination, amount, asset/unit, precision, fees, taxes, purpose, environment, adapter, and time limits are explicit.
- [ ] Required device, enrollment generation, workspace, repository, base commit, and expected-head bindings are explicit.
- [ ] Observed facts, interpretations, recommendations, disputed evidence, missing evidence, and privacy restrictions are separate.
- [ ] Decision states include `REVIEW_REQUIRED`, `INDETERMINATE`, `BLOCKED`, `DENIED`, `AUTHORIZED`, `EXPIRED`, `REVOKED`, `SUPERSEDED`, `DISPUTED`, `CORRECTED`, `WITHDRAWN`, and `UNKNOWN`.
- [ ] Material changes require a new review; prior records are never silently broadened or edited.
- [ ] Approval explicitly denies credential, custody, signing, capability, adapter, settlement, finality, publication, and release effects not separately granted.
- [ ] Expiry, correction, revocation, dispute, emergency stop, cache invalidation, consumer notification, acknowledgment, recovery, and residual risk are documented.
- [ ] Unreachable consumers and incomplete propagation remain blocking findings.
- [ ] Public review evidence excludes credentials, complete account identifiers, private device identifiers, private communications, and production transaction details.
- [ ] A reader can understand the exact decision and limitations without color, icons, diagrams, hidden interface state, or portfolio lore.

Evidence: _pending_

## P1C — Status, finality, and correction lifecycle

- [ ] Processing, authority, and evidence/finality status dimensions remain independent.
- [ ] `COMPLETED` processing does not imply financial authorization, adapter success, reconciliation, canonical acceptance, settlement, or legal finality.
- [ ] `AUTHORIZED` requires an approved independent authority and exact scope; it does not imply credentials, custody, adapter access, execution, settlement, or finality.
- [ ] `ADAPTER_REPORTED` is the strongest status an adapter may assign to itself.
- [ ] `RECONCILED`, `CANONICALLY_ACCEPTED`, and legal finality have separate owners and evidence requirements.
- [ ] Proposal-to-authorization, device-trust-to-authorization, submission-to-reconciliation, adapter-success-to-finality, and silent-scope-broadening transitions are prohibited.
- [ ] Partial, unknown, failed, reversed, refunded, disputed, corrected, expired, revoked, superseded, and withdrawn states remain visible and non-successful where applicable.
- [ ] Retry after an unknown outcome requires the original idempotency and replay domains and cannot duplicate effect.
- [ ] Corrections and revocations are append-only, invalidate dependent cached state, reach every registered consumer, and preserve the superseded generation.
- [ ] Unreachable or non-acknowledging consumers remain blocking findings.
- [ ] Every rendered status exposes object, scope, actor/owner or vacancy, observation time, uncertainty, active correction/revocation/dispute, and next permitted action in text.
- [ ] Lifecycle diagrams have complete prose equivalents and tables linearize for screen readers and zoom/reflow.
- [ ] The lifecycle guide is reviewed without being represented as an executable state machine, accepted status registry, financial authority, or finality determination.

Evidence: _pending_

## P1D — Consumer integration and conformance

- [ ] Consumer identity and exact implementation or documentation generation are explicit.
- [ ] Accepted profiles, record families, environments, authority effects, status dimensions, and reason-code registries are closed and versioned.
- [ ] Source identity, envelope, lineage, exact scope, and predecessor links are validated before interpretation.
- [ ] Parsing, rendering, transport, signatures, workflow success, or historical approval cannot create authority or compatibility.
- [ ] Processing, authority, and evidence/finality dimensions remain independent in storage and presentation.
- [ ] Scope intersection cannot broaden amount, destination, environment, adapter, device, workspace, repository, expected head, purpose, policy, or time window.
- [ ] Unknown profiles, unsupported records, malformed fields, missing bindings, substituted digests, and contradictory evidence fail closed.
- [ ] Retry after timeout or unknown outcome preserves the original idempotency and replay domains, prior evidence, retry budget, and duplicate-effect checks.
- [ ] Corrections, revocations, withdrawals, supersession, reversals, disputes, and emergency-stop records invalidate derivatives and remain append-only.
- [ ] Registered consumers acknowledge propagated changes within an approved time window; unreachable or non-acknowledging consumers remain blocking findings.
- [ ] Consumer-local projections identify source, exact scope, all status dimensions, actor/owner or vacancy, uncertainty, active corrections/revocations/disputes, next action, and non-canonical status.
- [ ] Positive and hostile fixture bytes are identical across participating repositories and include unsupported-profile, wrong-scope, stale, replay, duplicate, partial, unknown, corrected, revoked, unreachable-consumer, rollback, and restoration cases.
- [ ] Status and response rules are understandable without color, icons, diagrams, hover state, or hidden developer information.
- [ ] Privacy, minimization, retention, disclosure, deletion, audit, rollback, and restored-state requirements are explicit.
- [ ] The guide is reviewed without registering a consumer, accepting compatibility, or creating financial, capability, adapter, canonical, or legal authority.

Evidence: _pending_

## P2 — Future machine-readable compatibility evidence

Executable schemas and fixtures require separate approval.

- [ ] Canonical owner publishes immutable schemas, semantic profiles, canonical bytes, digest/signature scope, status registry, reason-code registry, transition rules, consumer-registration contract, and compatibility policy.
- [ ] Identical positive fixtures pass in every participating repository.
- [ ] Malformed, unsupported, stale, replayed, duplicate, wrong-identity, wrong-device, wrong-workspace, wrong-head, wrong-environment, wrong-adapter, over-limit, expired, revoked, and invalid-transition fixtures fail closed.
- [ ] Fixed-precision allocation, quote freshness, idempotency, partial failure, unknown outcome, timeout, retry, reversal, refund, dispute, correction, reconciliation, canonical-disposition, and finality vectors pass.
- [ ] Revocation and correction invalidate cached review state and every dependent capability and consumer projection.
- [ ] Lost-device and replacement-device fixtures preserve evidence and require fresh admissible bindings.
- [ ] Recovery restores a bounded state without deleting incident history or reactivating invalidated records.

Evidence: _pending; no executable contract is authorized_

## P3 — Exact-source documentation evidence

- [ ] Candidate commit and submitted head are immutable and recorded.
- [ ] Clean checkout, pinned dependencies, and `mkdocs build --strict` pass.
- [ ] Required files, navigation, and local links validate.
- [ ] Contract, consumer-integration, authorization-review, status/finality lifecycle, and accessibility guides appear in the rendered site.
- [ ] Pull-request workflow has read-only permissions and no Pages deployment, token-minting, payment, or infrastructure authority.
- [ ] Action and dependency identities, source archive, rendered site, source-identity record, SHA-256 manifests, and provenance record are retained.
- [ ] Generated output contains no credentials, account data, private device identifiers, network inventories, authorization records, or deployment secrets.
- [ ] Current exact-head evidence supersedes earlier runs without erasing historical results.

Evidence: _pending accepted exact-head result after the current documentation changes_

## Content, claims, and consistency

- [ ] Purpose and non-goals are consistent across README, Pages, task chain, punch list, release plan, and changelog.
- [ ] A.L.I.S.T.A.I.R.E. objective and QSO-PAYMENTS subsystem role are consistent.
- [ ] Proposal, validation, authorization review, authorization, capability, execution, adapter evidence, consumer projection, reconciliation, canonical disposition, dispute, custody, settlement, and legal finality are never conflated.
- [ ] A complete review record, trusted device, repository role, interface control, parsed record, completed stage, adapter report, passing workflow, or model recommendation is never described as financial authority or finality.
- [ ] No custody, signing, settlement-service, investment, suitability, certification, jurisdictional approval, or return promise is implied.
- [ ] Finality, pending, unknown, partial, reversal, dispute, correction, expiry, revocation, supersession, and withdrawal limitations are visible.
- [ ] Repository dependency descriptions and consumer integrations do not transfer authority.
- [ ] Architecture, contract, consumer integration, authorization-review, lifecycle/finality, accessibility, security/privacy, operations, release, and rollback documents receive human review.

Evidence: _pending_

## Accessibility and usability

- [ ] Heading structure, landmarks, navigation, link purpose, keyboard path, visible focus, contrast, and reduced motion reviewed.
- [ ] Tables and code blocks remain usable at 200% and 400% zoom and reflow without loss.
- [ ] Warnings, authority states, environments, device states, processing states, evidence/finality states, consumer states, and review states do not rely on color alone.
- [ ] Every meaningful diagram has equivalent prose.
- [ ] Every example is labeled documentation-only, illustrative, synthetic, or executable.
- [ ] A reader unfamiliar with the portfolio can identify proposer, validator, independent authorizer, capability issuer, adapter, consumer, reconciler, disposition owner, revoker, incident owner, unresolved evidence, finality limit, and prohibited effects.

Evidence: _pending_

## Security, privacy, and financial safety

- [ ] Source and rendered output scanned for secrets and sensitive personal, device, network, or financial data.
- [ ] External links, remote content, workflow supply chain, artifact retention, and publication risks reviewed.
- [ ] Self-approval, financial-authority/capability confusion, trusted-device/financial-permission confusion, cached authorization, invalid transition, replay, duplicate effect, adapter substitution, receipt forgery, consumer reinterpretation, and false-finality threats reviewed.
- [ ] Data minimization, tokenization, redaction, retention, disclosure, deletion, correction, revocation, and legal-hold rules reviewed.
- [ ] Automated budget escalation, self-funding loops, urgency overrides, and conflict-of-interest bypasses are prohibited.
- [ ] Incident contacts, containment authority, independent emergency disable, consumer notification, recovery order, and rollback owner are recorded.

Evidence: _pending_

## Publication, rollback, and approval

- [ ] Pages publication separately authorized.
- [ ] Published URL, deployed commit, claims, links, navigation, accessibility, security/privacy, and rollback route verified.
- [ ] Prior verified artifact identified and restoration credibly demonstrated.
- [ ] Correction or withdrawal updates every controlled documentation route and registered consumer declaration.
- [ ] Device loss, financial revocation, adapter disable, consumer invalidation, status correction, replacement-device, and recovery tabletop completed before any executable environment.
- [ ] Documentation, architecture, contract, integration, financial, legal/finality, security, privacy, accessibility, claims, device-trust, portfolio, recovery, and release reviewers approve their bounded responsibilities.

Decision: `BLOCKED`

Reason: Charter, independent financial authority, authority-source policy, device/workspace identity, Repository `1` role, schema/status/reason-code/transition and consumer-registration ownership, compatibility witnesses, exact-head review evidence, rendered accessibility review, legal/privacy/security review, publication approval, correction/revocation propagation, consumer acknowledgment, finality ownership, and recovery ownership remain pending. No simulation, testnet, adapter, device-control, consumer activation, or production payment work is authorized.
