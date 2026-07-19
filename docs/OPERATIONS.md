# Operations and recovery

The only currently authorized operational surface is the documentation site. These procedures govern building, reviewing, publishing, withdrawing, and restoring that site; they do not authorize payment adapters or external transfers.

## Publication pipeline

```text
Immutable candidate commit
    -> clean checkout
    -> pinned MkDocs install
    -> strict site build
    -> link / HTML / accessibility / claims / security review
    -> artifact hash and provenance record
    -> human release approval
    -> GitHub Pages deployment
    -> post-deployment verification
```

A deployment is not a release merely because GitHub Pages reports success.

## Local verification

```bash
python -m venv .venv
. .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements-docs.txt
mkdocs build --strict
```

Review the generated `site/` directory for unexpected files, sensitive content, broken navigation, misleading claims, and environment-label errors. Build output is disposable until tied to an immutable commit and retained as release evidence.

## Candidate evidence record

For each release candidate retain:

- repository URL, branch, tag if any, and exact commit SHA;
- workflow file digest and run identifier;
- Python, MkDocs, action, and runner versions;
- exact build and validation commands;
- link, HTML, accessibility, claims, privacy, security, and workflow-permission reports;
- source archive and generated-site artifact;
- SHA-256 manifest for retained artifacts;
- approver identities or roles and decision timestamps;
- deployed URL and post-deployment verification result;
- previous verified artifact and rollback procedure;
- unresolved findings and explicit release decision.

## Pre-publication checks

### Content and claims

- Confirm every capability is labeled documentation, simulation, testnet, or production.
- Confirm no page implies custody, signing, settlement, investment service, certification, legal approval, or guaranteed returns.
- Verify intent, authorization, allocation, adapter, receipt, reconciliation, and dispute remain distinct.
- Verify unresolved states and finality limitations are visible.

### Security and privacy

- Scan source and build output for secrets and sensitive identifiers.
- Review workflow permissions, checkout credential persistence, dependencies, and remote content.
- Confirm examples are fictional and contain no personal financial data.
- Confirm no restricted incident or adapter configuration evidence is published.

### Accessibility and usability

- Navigate the site with a keyboard.
- Verify visible focus, semantic headings, meaningful link text, readable tables, and zoom behavior.
- Check contrast and reflow at narrow widths.
- Ensure warnings and environment labels are understandable without color alone.

### Reproducibility

- Build from a clean checkout at the candidate SHA.
- Confirm the pinned requirements install successfully.
- Run `mkdocs build --strict` without warnings.
- Compare generated artifact hashes across equivalent clean builds or document expected nondeterminism.

## Deployment

The approved workflow builds the site and uploads the generated `site/` directory to GitHub Pages. Deployment permissions are limited to repository contents read, Pages write, and OIDC token issuance. The workflow must not receive payment credentials or adapter secrets.

After deployment:

1. verify the published commit and URL;
2. inspect primary navigation and every release-critical page;
3. repeat a focused accessibility and claims check;
4. record the deployment result and artifact hash;
5. keep the prior verified artifact available for rollback.

## Incident response

### 1. Detect and classify

Classify the incident as content/claim, privacy, credential, workflow/supply-chain, integrity/provenance, accessibility, or availability. If uncertainty exists, treat it as the higher-risk class until reviewed.

### 2. Contain

- Stop or disable the affected workflow when continued publication could worsen exposure.
- Withdraw the Pages artifact or restore the prior verified version.
- Revoke and rotate exposed credentials outside the repository if any secret was involved.
- Restrict incident evidence to approved reviewers.

### 3. Preserve evidence

Record commit SHAs, workflow runs, artifacts, hashes, timestamps, screenshots where safe, affected URLs, and reviewer observations. Do not rewrite history or delete evidence before preservation and secret-rotation decisions are complete.

### 4. Correct and verify

Prepare a narrowly scoped correction, rebuild from a clean checkout, repeat all affected checks, and document why the correction addresses the root cause. A content correction does not itself close a credential or privacy incident.

### 5. Recover and review

Publish only after explicit approval, verify the restored site, and record follow-up work in `taskchain.md`, `release.md`, `changelog.md`, or `punchlist.md` when one is approved.

## Rollback procedure

Rollback is required when the site materially overstates capability, leaks sensitive information, fails integrity checks, becomes inaccessible, or cannot be reproduced.

1. Identify the last verified artifact and commit.
2. Preserve the rejected candidate, reports, and hashes.
3. Redeploy the prior artifact or prior verified source commit.
4. Verify navigation, warnings, claims, and artifact identity.
5. Record the reason, affected interval, recovery evidence, and remaining investigation.
6. Do not mark the release gate complete merely because service was restored.

## Future adapter operations

Operational guidance for simulation, testnet, or production adapters is intentionally absent. Any future adapter requires a separate approved design covering secrets, authentication, request signing, replay resistance, rate limits, partial failure, finality, monitoring, reconciliation, incident response, disablement, and rollback. Documentation in this repository cannot activate that authority.
