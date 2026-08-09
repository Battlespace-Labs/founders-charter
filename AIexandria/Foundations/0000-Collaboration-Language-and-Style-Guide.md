# AIexandria Foundation 0000 — Collaboration Language and Style Guide

| Field | Value |
|---|---|
| Status | Draft |
| Classification | Foundation |
| Scope | AIexandria and UTOPIA collaboration |
| Revision policy | Append-only after adoption; supersede by reference |

## Purpose

Shared language is architecture. This guide defines a small, human-readable vocabulary for distinguishing edits, decisions, hypotheses, research tasks, and durable doctrine in human–AI collaboration. The notation is intentionally lightweight: prose remains primary, while explicit markers make intent discoverable and [machine-readable](https://en.wikipedia.org/wiki/Machine-readable_data).

Reference linking is governed by
[Doctrine 0001 — Document-Independent Reference Linking](../../Governance/Doctrine/0001-Document-Independent-Reference-Linking.md).
That adopted doctrine supersedes the former informal convention of linking only
the first meaningful occurrence of an unfamiliar term. This draft guide must be
read consistently with the controlling doctrine.

## Canonical vocabulary

- **AIexandria** is the canonical literal spelling. Do not silently change it to *Alexandria* or explain the wordplay unless the name itself is under discussion.
- **"Our Thing"** is written with capitalization and double quotation marks when used as the collaboration's recurring name.
- **UTOPIA** names the evolving knowledge architecture.
- **UoR** means Universe of Reality.
- **UoK** means Universe of Knowledge.
- **UoRᵐ** means a modeled reconstruction of reality, not reality itself.
- **Assertion** means a first-class, attributable, contextual, temporally scoped claim.
- **Temporal Substrate** means an execution and storage foundation in which [temporal database](https://en.wikipedia.org/wiki/Temporal_database) semantics are native rather than decorative metadata.
- **Doctrine** means an architectural principle expected to remain useful over a long horizon.
- **Constitution** means the maintained body of adopted foundational doctrine.

## Editorial markers

| Marker | Meaning |
|---|---|
| `@Edit` | Make a specific change to an existing artifact or concept. |
| `@Canonical` | Establish exact preferred wording or representation. |
| `@Rename` | Replace one name with another while preserving lineage. |
| `@Deprecated` | Retain for history but discontinue new use. |
| `@Alias` | Record a recognized alternate term without making it canonical. |
| `@Style` | Establish a presentation, punctuation, capitalization, or usage convention. |
| `@Retire` | Withdraw a concept or practice from active use, with rationale. |

Example:

```text
@Edit
Use AIexandria literally. Do not “correct” it to Alexandria.
```

## Intent markers

| Marker | Meaning | Expected treatment |
|---|---|---|
| `@Doctrine` | Durable foundational principle | Index, cross-reference, and test for contradictions |
| `@Hypothesis` | Plausible but unvalidated claim | Seek evidence and counterevidence |
| `@Decision` | Decision taken | Record rationale, scope, and consequences |
| `@ADR` | Architectural Decision Record | Preserve alternatives and decision history |
| `@Challenge` | Deliberate attempt to falsify a claim | Record tests and adverse evidence |
| `@Research` | Question requiring structured investigation | Track sources, findings, and confidence |
| `@Experiment` | Claim requiring implementation or measurement | Define method and success criteria |
| `@Question` | Open question not yet classified | Route to discussion or research |

Example:

```text
@Doctrine
No single representation, database, model, agent, or reasoning method optimally
satisfies every knowledge-system requirement.
```

## Informal discourse conventions

These conventions are useful signals, not rigid syntax:

- **Bold** highlights a candidate principle or statement requiring attention.
- “Double quotes” indicate exact wording, a named concept, or shared contextual language.
- ‘Single quotes’ indicate provisional, informal, or approximate terminology.
- ALL CAPS indicates an interruption or priority change, for example `BREAK BREAK`.
- Parenthetical remarks often carry qualification, history, humor, or important nuance.
- Ellipses indicate pacing or a held thought rather than necessarily uncertainty.

Explicit markers override inferred punctuation conventions.

## Processing model

AIexandria should eventually treat markers as semantic input. A parser or agent may:

1. identify the marked passage and its target;
2. create an immutable knowledge object for the stated intent;
3. index and cross-reference related assertions and doctrine;
4. flag contradiction, ambiguity, or missing evidence;
5. route research and experiment markers into tracked work;
6. preserve supersession and decision history;
7. nominate stable doctrine for the Constitution without adopting it automatically.

Human-readable meaning remains authoritative. Automation must not infer adoption merely because a marker exists.

## Foundation document lifecycle

Once adopted, foundation documents are append-only in the architectural sense: history must not be erased. A principle may be clarified, extended, deprecated, or superseded through a new, linked record.

Each document should record at least:

- status;
- adoption or proposal date;
- supersedes and superseded-by links;
- principle or purpose;
- motivation;
- implications;
- alternatives or challenges;
- open questions;
- related foundations.

Editorial corrections that do not alter meaning may be made in place. Substantive changes require an explicit revision or superseding document.

## Open questions

- Which markers are sufficiently distinct to remain in the core vocabulary?
- What grammar can be recognized reliably without making conversation unnatural?
- How should marker scope be expressed: sentence, paragraph, section, or referenced artifact?
- Which operations require human confirmation?
- How are contradictory markers from different members of a Community of Trust reconciled?
- Should marker history itself be represented as assertions in the UoK?

## Related foundations

- [0001 — No One Ring](0001-No-One-Ring.md)
- [0002 — Assertion-Centric Architecture](0002-Assertion-Centric-Architecture.md)
- [0003 — Temporal Substrate](0003-Temporal-Substrate.md)
- [0004 — Universe of Reality and Knowledge](0004-Universe-of-Reality-and-Knowledge.md)
- [0005 — Research Roadmap](0005-Research-Roadmap.md)
