# Accessibility and plain-language review

Status: **documentation candidate**

This guide defines how QSO-PAYMENTS documentation should be reviewed for accessibility, comprehension, and authority-state clarity. It does not certify conformance or authorize publication.

## Review objective

A reader must be able to determine—without relying on color, animation, iconography, financial expertise, or portfolio-specific shorthand—whether a described record is a proposal, validation, authorization, capability, adapter action, evidence item, reconciliation result, dispute, correction, or finality claim.

## Content structure

- Use one descriptive page title and a logical heading hierarchy.
- Put the environment and authority warning before procedural or architectural detail.
- Define specialized terms on first use and link to the contract reference.
- Keep paragraphs focused on one distinction or decision.
- Prefer explicit subjects and verbs: “the independent financial authority approves” rather than “approval occurs.”
- Mark unresolved ownership, evidence, or finality as unresolved rather than implying completion.
- State whether an example is documentation-only, simulation, testnet, or production.

## Status and authority labels

Every status must be expressed in text. A status badge, color, or diagram node may supplement the label but may not replace it.

Use the complete distinction when relevant:

```text
PROPOSED → VALIDATED → AUTHORIZED → ADMITTED → SUBMITTED → RECONCILED
```

The sequence is not automatic. Each arrow represents a separate decision or evidence boundary, and any stage may become rejected, expired, revoked, held, failed, unknown, partial, disputed, reversed, corrected, or superseded.

## Diagrams

Every meaningful Mermaid or other diagram requires nearby equivalent prose that identifies:

1. every component or actor;
2. the direction and meaning of each edge;
3. trust and authority boundaries;
4. failure, correction, revocation, and rollback paths;
5. unresolved decisions and prohibited inferences.

The prose must remain understandable if the diagram is unavailable. Do not encode meaning only by color, line style, position, shape, or animation.

## Tables

- Include a header for every column and row group.
- Avoid merged cells when a simple repeated label is clearer.
- Keep each cell meaningful when read independently.
- Explain abbreviations before the table.
- Ensure wide tables can scroll without clipping content.
- Provide a prose summary for tables that carry architectural or authority meaning.

## Links and navigation

- Use link text that describes the destination.
- Avoid “click here,” bare URLs, and repeated ambiguous labels.
- Keep the project overview, contract reference, architecture, onboarding, security/privacy, operations, release plan, and changelog reachable from the documentation front door.
- Identify external links and explain when an owning repository is authoritative.
- Mark historical or superseded evidence as historical or superseded in the link context.

## Code and record examples

- Label every example as illustrative, synthetic, or executable.
- Do not publish values that resemble live credentials, complete account numbers, private device identifiers, or production transaction references.
- Explain invalid placeholder digests or IDs so examples cannot be mistaken for accepted fixtures.
- Wrap or horizontally scroll long lines without hiding content.
- Provide a plain-language explanation after any example that carries semantic meaning.

## Keyboard and focus review

For the rendered site, verify:

- all interactive controls are reachable using a keyboard;
- focus order follows reading order;
- focus remains visible against the surrounding background;
- skip navigation or equivalent landmark navigation is available when provided by the theme;
- no content requires hover, drag, or pointer precision alone;
- external-link and copy controls do not trap focus.

## Zoom, reflow, and motion

- Review at 200% and 400% browser zoom.
- Confirm text reflows without horizontal scrolling except for tables and code blocks.
- Confirm warnings and status labels remain adjacent to the content they qualify.
- Respect reduced-motion preferences.
- Do not use motion as the only indication of state change.

## Plain-language authority test

A reviewer unfamiliar with the implementation should be able to answer:

- Who proposed the economic action?
- Who validated its structure and policy?
- Who independently authorized the financial scope?
- Who admitted the technical capability?
- Which adapter, environment, device, workspace, repository, and expected head were bound?
- What did the adapter report?
- What remains pending, unknown, partial, disputed, or reversible?
- Who may correct, revoke, stop, reconcile, recover, and approve release?
- What has not been implemented or authorized?

If any answer depends on inference, color, portfolio lore, or a missing owner, the documentation is not review-ready.

## Review evidence checklist

- [ ] Heading and landmark structure reviewed.
- [ ] Keyboard path and visible focus reviewed.
- [ ] Link purpose and navigation reviewed.
- [ ] Tables and code blocks reflow or scroll safely.
- [ ] Contrast reviewed.
- [ ] 200% and 400% zoom reviewed.
- [ ] Reduced-motion behavior reviewed.
- [ ] Diagrams have equivalent prose.
- [ ] Status and authority distinctions do not rely on color alone.
- [ ] Documentation-only, simulation, testnet, and production states are explicit.
- [ ] Proposal, validation, authorization, capability, execution, receipt, reconciliation, and finality are understandable without domain expertise.
- [ ] Public examples contain no sensitive or production-like data.
- [ ] Findings are linked to the exact source commit and rendered artifact.
- [ ] Corrections and withdrawals identify every affected documentation route.

## FYSA-120 capability mapping

This review surface applies CAT-011 for visual and cross-modal integrity, CAT-012 for information architecture and technical editing, CAT-019 for accessible plain-language communication, CAT-031 for reviewable validation evidence, and CAT-040 for correction and withdrawal continuity.

Proposed non-authoritative subdivision: **`019-I — authority-state accessibility and financial-interface comprehension review`**.

## Authority boundary

Completing this checklist is evidence for documentation review only. It is not an accessibility certification, financial approval, legal opinion, release approval, Pages publication authorization, or production-readiness decision.
