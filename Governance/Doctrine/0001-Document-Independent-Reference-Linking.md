# Doctrine 0001 — Document-Independent Reference Linking

| Field | Value |
| --- | --- |
| Status | Adopted doctrine |
| Adopted | 2026-08-09 |
| Scope | Battlespace Labs-authored, human-facing durable artifacts across repositories |
| Supersedes | Prior informal first-meaningful-occurrence convention; no durable locator |
| Related | [AIexandria Foundation 0000 — Collaboration Language and Style Guide](../../AIexandria/Foundations/0000-Collaboration-Language-and-Style-Guide.md) |

## Doctrine

Battlespace Labs artifacts must be understandable without presuming that a
reader has encountered any other document, repository, section, or earlier use
of a term.

Authors and editors must provide active
[reference links](https://en.wikipedia.org/wiki/Hyperlink) for
[acronyms](https://en.wikipedia.org/wiki/Acronym), specialized terms, and
technical, scientific, philosophical, historical, or otherwise unfamiliar
concepts whenever a definition would reasonably aid comprehension. The
threshold for adding a useful link is deliberately low.

Reference sufficiency is evaluated at the independently readable artifact or
entry point—not once for an entire repository, series, or presumed reading
sequence. A first-use-only check is therefore never sufficient by itself.

## Reference authority

### Internally developed or defined terms

Link an internally developed acronym, term, or concept to its fullest current
definition in a Battlespace Labs repository. Prefer the canonical definition
over a passing mention, index entry, conversation, or abbreviated summary.

When definitions evolve, link the currently controlling definition and preserve
the predecessor's supersession path. A reference link does not change which
repository owns the concept or elevate working material into doctrine.

### External terms and concepts

Link an external term or concept to its corresponding
[Wikipedia](https://en.wikipedia.org/wiki/Wikipedia) article whenever a suitable
article exists. A governing standard, primary source, or specialist reference
may be linked in addition when precision requires it.

When Wikipedia has no suitable article, use the most authoritative accessible
definition available and make the exceptional target clear. Do not substitute a
vendor homepage, search result, or passing use for a full definition.

## Application rules

1. Expand an acronym and link it wherever an independently arriving reader may
   otherwise lack the definition.
2. Place the active link on the term, acronym, or immediately adjacent
   definition rather than relying only on a bibliography or unlinked glossary.
3. Repeat links when useful. Link economy is subordinate to comprehension,
   especially in independently addressable sections, tables, diagrams,
   captions, appendices, presentations, and generated views.
4. Treat a local glossary as a navigation aid, not an exemption from contextual
   links at likely entry points.
5. Use descriptive targets that lead to the full definition and remain useful
   outside the author's current browsing context.
6. Review technical, scientific, philosophical, and historical concepts with a
   presumption in favor of linking when reasonable readers may differ in
   familiarity or interpretation.

Common vocabulary need not be linked merely to maximize link count. The test is
whether a definition materially reduces ambiguity, hidden prerequisite
knowledge, or interruption of comprehension; close cases favor a link.

## Format and boundary exceptions

- Preserve quotations and immutable source material exactly; supply any needed
  reference in surrounding editorial text.
- When code, a schema, or a
  [machine-readable](https://en.wikipedia.org/wiki/Machine-readable_data) format
  cannot carry a usable active link, provide the reference in its human-facing
  documentation or supported [metadata](https://en.wikipedia.org/wiki/Metadata)
  field.
- Do not expose a private repository, restricted concept, or sensitive locator
  merely to satisfy this doctrine. A public artifact that depends on a private
  definition must either link an approved public definition or state the access
  limitation without disclosing protected material.
- Link targets must respect the existing public/private and artifact-authority
  boundaries of Battlespace Labs repositories.

## Conformance and transition

This doctrine applies immediately to new artifacts and material revisions.
Existing artifacts should be brought into conformance through bounded,
reviewable changes, prioritized by readership, conceptual density, and risk of
misunderstanding. Adoption does not authorize bulk rewriting, deletion, or a
change in publication classification.

Reviewers should inspect each artifact as if entered directly rather than read
in repository order. Review includes checking link relevance, accessibility,
canonical ownership, and obvious breakage.

## Supersession statement

This doctrine supersedes any informal convention that limited explanatory links
to the first meaningful occurrence of a term. Prior occurrence elsewhere does
not discharge the duty to make the current artifact or independently readable
entry point intelligible.

The earlier convention had no durable repository locator. Its replacement is
recorded here so future guidance can cite and supersede an authoritative text.
