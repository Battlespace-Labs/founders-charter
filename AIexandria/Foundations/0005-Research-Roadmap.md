# AIexandria Foundation 0005 — Research Roadmap

| Field | Value |
|---|---|
| Status | Initial roadmap |
| Classification | Research program |

## Purpose

This roadmap converts the initial AIexandria/UTOPIA foundations into [falsifiable](https://en.wikipedia.org/wiki/Falsifiability) research, executable prototypes, and evidence-backed architectural decisions. It intentionally preserves open questions rather than treating an energetic architectural discussion as settled science or demonstrated novelty.

## Research principles

1. Separate verified facts, architectural judgments, hypotheses, and aspirations.
2. Search for prior art before claiming novelty.
3. Attempt to falsify the strongest ideas.
4. Prefer small executable experiments over speculative platform construction.
5. Benchmark logical correctness and provenance fidelity as well as speed.
6. Preserve negative findings; eliminating an idea is progress.
7. Treat products as replaceable candidates evaluated against role-specific requirements.

## Workstream A — Formal assertion model

### Questions

- What is the minimum complete structure of an assertion?
- How are n-ary propositions, nested claims, contradiction, support, and supersession represented?
- How do identity, semantics, assertions, state, and presentation remain separate?
- How are confidence and uncertainty calibrated and propagated?

### Outputs

- implementation-independent metamodel;
- normative examples drawn from CTI;
- validation rules and competency questions;
- mappings to STIX 2.1, MISP, UCO/RDF, property graphs, and typed relation models;
- documented information-loss cases.

## Workstream B — Multitemporal and epistemic semantics

### Questions

- Which temporal axes are core versus extensible?
- How are uncertain intervals and differing precision represented?
- What query algebra distinguishes current reconstruction from historical belief?
- How is temporal scope computed for derived assertions?

### Outputs

- temporal type system;
- Allen-style interval algebra profile;
- query semantics for current, point-in-knowledge-time, interval, and retrospective projections;
- late-arriving-data and supersession test corpus;
- temporal inference conformance tests.

## Workstream C — UoR, UoK, and Community of Trust

### Questions

- Can UoR, UoK, and UoRᵐ be expressed operationally and formally?
- How are observer-specific and community-specific beliefs represented?
- What constitutes acceptance, consensus, or authoritative status?
- How can a historical decision be reconstructed without hindsight leakage?

### Outputs

- formal definitions and counterexamples;
- community/context model;
- reproducible worldview projection specification;
- incident case studies comparing present understanding with historical belief.

## Workstream D — Polyglot architecture and semantic contracts

### Questions

- Can one logical model generate faithful typed, RDF/OWL, property-graph, columnar, and document projections?
- Which store is authoritative for which artifact?
- Can assertion identity and provenance survive round trips?
- What consistency and recovery guarantees are operationally required?

### Candidate evaluations

Evaluate roles rather than declare a universal winner. Candidate families include:

- typed conceptual and reasoning databases;
- RDF/OWL semantic stores;
- embedded or distributed property-graph engines;
- relational and columnar analytical systems;
- immutable object and evidence stores;
- vector and full-text retrieval systems.

Current product names should be selected and verified during the evaluation; foundation doctrine must not depend on their continued availability.

### Outputs

- role-based requirements matrix;
- projection and round-trip prototypes;
- failure-mode analysis;
- architecture decision records based on evidence.

## Workstream E — Performance and scalability

### Hypotheses

- Native temporal planning outperforms application-level historical reconstruction at scale.
- Selective physicalization provides most of the benefit of materialized temporal relations without quadratic growth.
- Current and historical knowledge projections can be incrementally maintained.
- Specialized analytical projections can be regenerated without becoming competing authorities.

### Benchmark dimensions

- assertion count, evidence fan-in, and relationship arity;
- number and density of temporal intervals;
- late arrivals, revisions, contradictions, and supersessions;
- community and context cardinality;
- point-in-time and interval reconstruction latency;
- temporal inference cost;
- storage amplification;
- provenance completeness and semantic fidelity;
- recovery, replay, and reproducibility.

## Workstream F — Prior art, publication, and intellectual property

Conduct structured review across:

- [bitemporal](https://en.wikipedia.org/wiki/Temporal_database) and multitemporal databases;
- temporal and dynamic knowledge graphs;
- [event sourcing](https://en.wikipedia.org/wiki/Event_sourcing) and immutable data systems;
- [belief revision](https://en.wikipedia.org/wiki/Belief_revision) and truth-maintenance systems;
- provenance models and argumentation frameworks;
- probabilistic, causal, and [neuro-symbolic AI](https://en.wikipedia.org/wiki/Neuro-symbolic_AI) reasoning;
- temporal logics, Event Calculus, and interval algebras;
- CTI standards and historical intelligence-analysis systems;
- relevant patents and published applications.

Maintain a **Candidate Novel Concepts** register with:

- precise description;
- suspected novelty;
- closest known prior art;
- differentiating mechanism;
- evidence and counterevidence;
- confidence;
- publication and disclosure status;
- unresolved questions.

Publication should be used to force precision. Patent decisions require qualified legal advice and should follow, not substitute for, technical definition and prior-art analysis.

## Workstream G — Collaboration language

Prototype the markers in Foundation 0000 against real conversations and documents.

Measure:

- human usability;
- parsing precision and recall;
- ambiguity of marker scope;
- contradiction detection;
- traceability from conversation to adopted doctrine;
- confirmation requirements for consequential edits.

The result may become a lightweight knowledge-engineering language, but that remains a hypothesis.

## Initial sequence

### Phase 0 — Preserve and define

- review and adopt or revise Foundations 0000–0005;
- assemble source discussions and earlier UTOPIA papers as provenance;
- define document lifecycle and decision-record templates.

### Phase 1 — Specify

- produce the assertion metamodel and temporal type system;
- define competency questions and CTI scenarios;
- formalize UoR/UoK/UoRᵐ terminology.

### Phase 2 — Prototype

- implement the same bounded scenario in at least two different storage families;
- generate current and historical knowledge views;
- verify round-trip provenance and assertion identity.

### Phase 3 — Challenge and benchmark

- run falsification exercises and prior-art review;
- benchmark native and emulated temporal strategies;
- document failure modes and revise the model.

### Phase 4 — Decide and publish

- record evidence-backed architecture decisions;
- publish the conceptual model and benchmark method where appropriate;
- identify any genuinely novel mechanisms for separate legal evaluation.

## Near-term demonstration scenario

Use one compact CTI incident with:

- an event whose occurrence time is initially uncertain;
- sensor observation and later analyst detection;
- two conflicting attribution assertions;
- publication and receipt by another Community of Trust;
- later evidence that changes the estimated event interval and attribution;
- a decision made using only the evidence available at that historical time.

The prototype must answer:

1. What do we believe now happened?
2. What did each community believe at a specified time?
3. How and why did confidence change?
4. Which evidence and inference supported each view?
5. Can the historical decision be replayed without later evidence?
6. Can all answers be reproduced across multiple physical projections?

## Exit criteria for the initial research cycle

- Terms are defined sufficiently to produce independent implementations.
- At least one strong claim has survived deliberate falsification.
- At least one strong claim has been narrowed, corrected, or rejected.
- Two physical representations answer the competency questions with documented fidelity.
- Performance measurements distinguish native benefits from modeling convenience.
- Prior-art findings bound any novelty claim.
- The next architecture decisions are supported by evidence rather than product enthusiasm.

## Related foundations

- [0000 — Collaboration Language and Style Guide](0000-Collaboration-Language-and-Style-Guide.md)
- [0001 — No One Ring](0001-No-One-Ring.md)
- [0002 — Assertion-Centric Architecture](0002-Assertion-Centric-Architecture.md)
- [0003 — Temporal Substrate](0003-Temporal-Substrate.md)
- [0004 — Universe of Reality and Knowledge](0004-Universe-of-Reality-and-Knowledge.md)
