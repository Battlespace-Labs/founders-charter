# AIexandria Knowledge Workflow

This directory implements
[Doctrine 0002 — Human-Centered Knowledge Workflow](../../Governance/Doctrine/0002-Human-Centered-Knowledge-Workflow.md).
It is the agent-facing infrastructure behind the rich documents in
[AIexandria Dossiers](../Dossiers/).

## Human experience

Humans should normally:

1. discuss, research, decide, design, or provide source material naturally;
2. read and correct the subject's dossier;
3. confirm only consequential decisions or changes in authority.

Humans are not expected to maintain the objects, schemas, or inventory in this
directory.

## Agent contract

For each material contribution, an agent should:

1. resolve an existing concept identity before creating another;
2. capture only as much structure as the concept currently warrants;
3. preserve provenance, temporal context, distinctions, and supersession;
4. update the machine object and its primary human view together;
5. validate changed structured artifacts;
6. request human confirmation for adoption, retirement, destructive change, or
   a material change to meaning or scope.

An agent must not treat schema conformance as proof that a claim is true or that
a decision has been adopted.

## Directory map

| Path | Purpose |
| --- | --- |
| [`schemas/knowledge-object.schema.json`](schemas/knowledge-object.schema.json) | Minimal common envelope for agent-managed knowledge objects |
| [`objects/`](objects/) | Structured concept records with stable identities and provenance |
| [`inventory/repository-artifacts.json`](inventory/repository-artifacts.json) | Current and unresolved artifact locations used for migrate-on-touch transition |
| [`../Dossiers/`](../Dossiers/) | Primary human-facing subject views |

## Object lifecycle

| State | Meaning |
| --- | --- |
| `captured` | Preserved with minimal interpretation |
| `working` | Actively shaped; meaning or design may still change |
| `adopted` | Explicitly authorized within its stated scope |
| `superseded` | Retained for lineage but replaced by a linked successor |
| `retired` | Retained for history and intentionally withdrawn from active use |

Lifecycle state, maturity, and truth are separate. A fully structured object may
still represent a hypothesis; an adopted decision may remain technically simple.

## Pilot

[Ideation Capture](../Dossiers/Ideation-Capture.md) is the first complete
substrate-plus-dossier pilot. Its machine record deliberately distinguishes it
from the separate audiobook cognition/sleep-detection application concept.
