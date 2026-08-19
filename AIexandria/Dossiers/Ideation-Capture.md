# Ideation Capture — Project Dossier

| Field | Current value |
| --- | --- |
| Status | Working design; purpose and scope separation confirmed |
| Durable identity | `bsl:idea:ideation-capture` |
| Primary owner | Patrick Maroney / Battlespace Labs |
| Last integrated | 2026-08-19 |
| Governing workflow | [Doctrine 0002 — Human-Centered Knowledge Workflow](../../Governance/Doctrine/0002-Human-Centered-Knowledge-Workflow.md) |
| Machine record | [Ideation Capture knowledge object](../Knowledge/objects/ideas/ideation-capture.json) |

## Executive view

Ideation Capture is the capability through which a person can express an idea
naturally and rely on agents to preserve, reconnect, develop, and present it.
The human experience is conversation and a rich living dossier. Stable
identity, schemas, relationships, provenance, lifecycle, and validation remain
behind that interface.

The design exists to remove a failure mode we encountered directly: the
recordkeeping method became more demanding than the thinking it was meant to
support. The correction is not to abandon structure. It is to place structure
at the proper abstraction layer.

> Capture should feel effortless; structure should remain rigorous.

This is the Ideation Capture expression of the
[Invisible Machinery Principle](../../Governance/Doctrine/0002-Human-Centered-Knowledge-Workflow.md#invisible-machinery-principle):
“You supply the ideas; the machinery should increasingly disappear underneath
us.” Pat approves consequences, not mechanics. The agent-managed substrate
remains inspectable, provenance-aware, validated, and recoverable even as its
routine operation recedes from the human experience.

## Scope boundary

Ideation Capture is independent of sleep state.

It is intentionally distinct from the proposed Apple Watch-enabled application
that detects when an audiobook listener has fallen asleep or otherwise lost
cognitive engagement. That application is a separate idea. Ideation Capture
will be used to memorialize, refine, and extend it without merging their
identities.

| Ideation Capture | Audiobook cognition detection |
| --- | --- |
| Captures and develops ideas from human activity | Detects probable loss of engagement during listening |
| Independent of sleep or physiology | Depends on watch/phone sensors and inference |
| General Battlespace Labs knowledge capability | Specific product/application concept |
| Produces dossiers and linked knowledge objects | May consume Ideation Capture for its own design history |

## Intended experience

Patrick speaks, types, uploads, sketches, or points to source material. The
agent determines whether the contribution extends an existing subject, captures
its provenance, updates the minimum necessary structure, and refreshes the
subject dossier.

The normal interaction does **not** require Patrick to:

- choose `idea`, `decision`, `assertion`, or another object class;
- complete a template before thinking aloud;
- author or inspect JSON;
- maintain indexes, identifiers, timestamps, or relationship edges;
- decide which repository path owns every contribution;
- reconstruct a topic from multiple session histories.

Explicit markers such as `@Decision` or `@Research` remain available when they
help communicate intent, but they are optional.

## Operating model

| Stage | Agent responsibility | Human involvement |
| --- | --- | --- |
| Capture | Preserve the contribution and source context | Express the idea naturally |
| Resolve | Match or create a persistent concept identity | Clarify only genuine ambiguity |
| Structure | Add the minimum useful type, state, relationships, and provenance | None for routine classification |
| Develop | Connect evidence, decisions, designs, questions, and actions | Think, judge, and redirect |
| Render | Maintain one coherent primary dossier and any warranted formal deliverables | Read and correct the human view |
| Govern | Preserve lineage and validate artifacts | Confirm consequential decisions |

## Authority and confirmation

Agents may perform routine capture, classification, cross-linking, formatting,
validation, and dossier maintenance. Human confirmation is required before:

- adopting doctrine or a material decision;
- materially changing a concept's purpose, scope, ownership, or authority;
- retiring or destructively replacing a durable artifact;
- resolving genuinely competing identities when the merge could erase a
  meaningful distinction.

A schema-valid object is not automatically true, approved, or adopted.

## Information model

The pilot uses a deliberately small common envelope defined by the
[AIexandria Knowledge Object schema](../Knowledge/schemas/knowledge-object.schema.json).
It records:

- stable identity and object type;
- a concise summary;
- lifecycle state, maturity, and authority;
- created and updated times;
- typed relationships;
- source provenance;
- human-facing views;
- a domain-specific payload.

This is an extensible envelope, not a universal ontology or a frozen assertion
model. Additional domain schemas should be introduced only when evidence shows
they provide value.

## Inputs and outputs

### Candidate inputs

- natural-language conversations and spoken notes;
- documents, links, research results, and source files;
- photographs of whiteboards and journal pages;
- decisions, challenges, experiments, and implementation work;
- corrections made directly to a dossier.

### Primary outputs

- one persistent identity for the concept;
- one primary, well-composed subject dossier;
- linked decisions, assertions, evidence, designs, questions, and actions;
- specialized reports, specifications, presentations, or code when maturity
  warrants them;
- provenance and lineage sufficient to reconstruct meaningful evolution.

## Relationship to other AIexandria artifacts

| Artifact | Role |
| --- | --- |
| [Foundation 0000](../Foundations/0000-Collaboration-Language-and-Style-Guide.md) | Supplies optional collaboration vocabulary and markers |
| [Foundation 0002](../Foundations/0002-Assertion-Centric-Architecture.md) | Governs first-class assertions and non-destructive knowledge evolution |
| Session Continuity Object | Carries transient working state across sessions; does not own domain truth |
| Cassandra | Becomes a generated chronological and interpretive view rather than a manually maintained journal |
| GitHub | Preserves adopted artifacts, implementation history, review, and governance |
| Future presentation workspace | May render and edit dossiers without becoming the underlying data model |

The durable locations of the earlier Session Continuity Object package and
Cassandra artifacts remain unresolved. They are preserved as explicit
inventory entries for migrate-on-touch treatment rather than being silently
recreated or discarded.

## Decisions and rationale

| Date | Decision | Rationale |
| --- | --- | --- |
| 2026-08-04 | Keep Ideation Capture independent of audiobook cognition detection | They solve different problems and require different artifacts |
| 2026-08-04 | Develop Ideation Capture first and use it to memorialize the audiobook concept | The general capture capability can preserve the product's continuing design |
| 2026-08-11 | Keep schemas and structured objects, but move their operation behind the human interface | Structure is valuable; manual schema operation was overwhelming the work |
| 2026-08-11 | Use rich dossiers as the primary human reading surface | A subject should be understandable without reconstructing scattered machine records |
| 2026-08-11 | Preserve and migrate on touch | Avoids both information loss and a disruptive all-at-once conversion |
| 2026-08-19 | Name the Invisible Machinery Principle and preserve “Pat approves consequences, not mechanics” | Makes the intended division of labor explicit while retaining inspectability, provenance, validation, and recovery |

## Pilot acceptance criteria

The pilot succeeds when:

1. a normal conversation can extend this concept without requiring a form;
2. the agent can find and update the existing identity rather than creating a duplicate;
3. the machine object validates and retains source provenance;
4. this dossier remains the coherent human view of current understanding;
5. consequential changes are visible and confirmed;
6. the separate audiobook concept remains separate but linked;
7. unresolved historical artifacts remain discoverable until reconciled.

## Open questions

- Which additional capture channel should follow conversation and files:
  voice-first notes, whiteboards, journal pages, or another source?
- What confidence threshold permits automatic concept matching?
- Which human dossier edits can be reconciled automatically without risking a
  change to adopted meaning?
- When this pilot outgrows the founders-charter repository, which repository or
  knowledge store should own operational objects?
- What is the smallest useful domain schema beyond the common envelope?

## Next actions

1. Use this dossier and object during the next substantive Ideation Capture discussion.
2. Memorialize the audiobook cognition-detection concept as a separate linked object and dossier.
3. Reconcile the previously created ideation and Session Continuity Object artifacts when their authoritative copies are located.
4. Evaluate the pilot after real use before adding more schema or workflow machinery.

## Lineage note

This dossier integrates the August 4, August 11, and August 19, 2026 decisions.
It does not claim to be a wholesale migration of prior conversations. The
[artifact inventory](../Knowledge/inventory/repository-artifacts.json) records
what is authoritative here and what remains unresolved so future work can
extend the concept without erasing its history.
