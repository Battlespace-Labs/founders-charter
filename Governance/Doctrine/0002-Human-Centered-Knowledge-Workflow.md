# Doctrine 0002 — Human-Centered Knowledge Workflow

| Field | Value |
| --- | --- |
| Status | Adopted doctrine |
| Adopted | 2026-08-11 |
| Refined | 2026-08-19 — Invisible Machinery Principle |
| Scope | Battlespace Labs and AIexandria knowledge capture, management, and presentation |
| Implements | Knowledge workflow reset directed 2026-08-11 |
| Related | [AIexandria Foundation 0000 — Collaboration Language and Style Guide](../../AIexandria/Foundations/0000-Collaboration-Language-and-Style-Guide.md) |

## Doctrine

> Humans work with ideas, decisions, designs, evidence, and documents. Agents
> manage object structure, schemas, validation, lineage, and rendering.

Battlespace Labs separates the human collaboration experience from the
[machine-readable](https://en.wikipedia.org/wiki/Machine-readable_data)
knowledge substrate. Conversation and rich, independently readable documents
are the normal human interfaces. Structured objects and schemas remain
essential infrastructure, but their routine maintenance belongs to agents and
automation.

The purpose of structure is to increase continuity, trust, reuse, and
reasoning—not to impose clerical work on the human collaborator.

## Operating principles

1. **Conversation first.** Natural discussion is a valid capture interface.
   Humans need not select an object type, complete a form, or choose a storage
   location before developing an idea.
2. **One persistent identity per concept.** Later discussion normally refines
   the existing concept. It does not create a disconnected artifact merely
   because it occurred in another session, device, model, or tool.
3. **Progressive formalization.** An item receives only the structure warranted
   by its maturity, consequence, and expected reuse.
4. **Agents maintain the substrate.** Agents infer candidate classifications,
   resolve identities, update relationships, preserve provenance, validate
   schemas, and render human views.
5. **One primary dossier per subject.** A subject may require many underlying
   objects, sources, and formal deliverables, but it should normally offer one
   coherent [dossier](https://en.wikipedia.org/wiki/Dossier) as its principal
   human reading surface.
6. **Consequential decisions require human confirmation.** Routine capture,
   classification, formatting, cross-linking, and validation may be automatic.
   Adoption, retirement, material scope change, destructive replacement, or a
   change to governing doctrine requires explicit human authority.
7. **Lineage is mandatory; bureaucracy is not.** Meaningful changes retain
   provenance and supersession paths without forcing humans to operate the
   recordkeeping machinery.
8. **Migration occurs on touch.** Existing material is preserved, inventoried,
   and reconciled when its subject is next used. Useful work does not wait for a
   wholesale historical conversion.

## Invisible Machinery Principle

> You supply the ideas; the machinery should increasingly disappear underneath
> us.

Pat approves consequences, not mechanics. Once an objective and its boundaries
are authorized, agents should handle routine capture, classification,
cross-linking, validation, reconciliation, preservation, and review mechanics
without transferring their operational burden back to Pat. Human attention is
reserved for meaning, judgment, correction, and consequential choices.

Invisible does not mean opaque. The underlying machinery must remain rigorous,
inspectable, provenance-aware, and recoverable. Its work should leave enough
evidence and lineage to explain what happened, validate the result, correct an
error, or restore prior state. What disappears is routine complexity at the
human interface—not accountability or control.

This principle names and reconciles operating principles 3, 4, 6, and 7:
formalization remains proportional; agents maintain the substrate; humans
confirm consequences; and lineage remains mandatory without becoming human
bureaucracy.

## Two-layer model

| Layer | Primary users | Responsibilities | Normal artifacts |
| --- | --- | --- | --- |
| Human-facing knowledge | Founders, collaborators, reviewers, readers | Understanding, judgment, correction, decision, communication | Dossiers, reports, specifications, presentations, decision records |
| Machine knowledge substrate | Agents, validators, renderers, retrieval and reasoning services | Identity, typing, relationships, lifecycle, temporality, provenance, validation, synchronization | Structured objects, schemas, indexes, manifests, lineage records |

The layers are connected but not interchangeable. A raw structured object is
not an adequate human deliverable. A polished document does not eliminate the
need for identity, provenance, and machine-operable relationships.

## Authority by facet

No single file format or platform is authoritative for every concern. Authority
is assigned by facet:

| Facet | Authority |
| --- | --- |
| Normative policy and adopted wording | The controlling adopted human-readable doctrine or decision record |
| Concept identity, relationships, provenance, and lifecycle state | The validated machine knowledge object and its lineage |
| Original evidence or source content | The preserved source artifact |
| Current integrated human understanding | The subject's primary dossier, reconciled with the substrate |
| Session handoff state | A [Session Continuity Object](../../AIexandria/Knowledge/inventory/repository-artifacts.json), which never replaces domain truth |

When a human edit and a machine object disagree, an agent must reconcile the
facets rather than silently choosing a winner. A change to adopted meaning is
escalated for human confirmation.

## Human-facing document requirements

A primary dossier should be useful without exposing implementation mechanics.
It should normally provide:

- purpose and current understanding;
- adopted decisions and their rationale;
- important ideas, designs, and evidence;
- open questions, risks, and assumptions;
- current actions and priorities;
- relevant sources and formal deliverables;
- a concise history of meaningful evolution.

Object identifiers, schema details, and validation state may appear in a
technical appendix or link, but they are not the main reading experience.

## Agent responsibilities

For material knowledge work, an agent should:

1. capture the relevant contribution and its provenance;
2. resolve whether it extends an existing concept;
3. create or update the minimum necessary structured object;
4. preserve distinctions, contradictions, and supersession rather than flattening them;
5. render or update the subject's human-facing dossier;
6. request confirmation only when authority, meaning, scope, or risk requires it;
7. validate machine artifacts and links before proposing repository changes.

Editorial markers from
[Foundation 0000](../../AIexandria/Foundations/0000-Collaboration-Language-and-Style-Guide.md)
remain useful explicit signals. They are optional accelerators, not a syntax
that humans must use for successful capture.

## Preservation and transition

Existing artifacts and repository history must not be discarded merely because
the workflow changes. Transition follows this sequence:

1. preserve the original artifact and its history;
2. inventory its known location and role;
3. classify it as current, source material, duplicate, superseded, or unresolved;
4. identify the best current authority without manufacturing certainty;
5. migrate and reconcile the subject when it is next touched;
6. record derivation, replacement, and supersession links.

This doctrine does not authorize bulk rewriting, deletion, silent adoption, or
the consolidation of every knowledge function into one platform. It implements
the composable architecture required by
[AIexandria Foundation 0001 — No One Ring](../../AIexandria/Foundations/0001-No-One-Ring.md).

## Initial implementation

The first implementation slice is
[Ideation Capture](../../AIexandria/Dossiers/Ideation-Capture.md). It pairs a
rich human dossier with a validated
[machine knowledge object](../../AIexandria/Knowledge/objects/ideas/ideation-capture.json)
and uses the
[repository artifact inventory](../../AIexandria/Knowledge/inventory/repository-artifacts.json)
to preserve unresolved prior material without blocking current work.

## Conformance test

The workflow conforms when a founder can develop and revisit a subject through
normal conversation and a coherent dossier while agents can independently
locate its identity, provenance, relationships, status, governing decisions,
and source lineage.

If the human must routinely manipulate JSON, select schemas, maintain indexes,
or reconstruct a subject from scattered records, the implementation does not
conform even if its machine artifacts validate.
