# AIexandria Foundation 0002 — Assertion-Centric Architecture

| Field | Value |
|---|---|
| Status | Draft doctrine |
| Classification | Logical architecture |

## Doctrine

> The foundational knowledge unit is an assertion, not merely a node, edge, property, document, or current state.

An assertion is a first-class, identifiable claim made by an observer or agent about a subject, relationship, event, process, classification, or other modeled phenomenon. It lives in the Universe of Knowledge while referring toward a proposed feature of the Universe of Reality. In this sense, assertion-centric modeling is an [epistemological](https://en.wikipedia.org/wiki/Epistemology) commitment as well as a data-modeling choice.

## Why assertion primacy

Facts encountered in CTI are rarely context-free. A claim may be supported, contradicted, revised, accepted by one community, rejected by another, or superseded as evidence changes. Confidence, provenance, temporal scope, and method belong to the claim—not automatically to the entity or event the claim describes.

Making assertions first-class allows the system to preserve disagreement and intellectual history without rewriting the past.

## Conceptual form

An assertion minimally relates:

```text
asserter + proposition + referent + context + temporal scope + provenance
```

The proposition may be expressed through subject–predicate–object form, an [n-ary relation](https://en.wikipedia.org/wiki/Finitary_relation), a structured event, a hypothesis, a classification, or another typed semantic construct. The architecture must not reduce every claim to a binary edge when the domain is intrinsically n-ary.

## Candidate assertion facets

| Facet | Purpose |
|---|---|
| Identity | Stable reference to this assertion |
| Proposition | What is claimed |
| Asserter | Person, organization, sensor, process, or agent making the claim |
| Evidence | Observations or other assertions offered in support |
| Provenance | Source, acquisition, transformations, and custody |
| Context | Scope, community, case, analytic frame, and assumptions |
| Confidence | Calibrated degree and method, not a decorative percentage |
| Reality scope | When the claimed phenomenon is believed to hold or occur |
| Knowledge history | When the assertion was created, published, received, adopted, revised, or superseded |
| Classification and handling | Access, sharing, and policy constraints |
| Status | Proposed, accepted, challenged, withdrawn, superseded, or another typed state |
| Derivation | Rules, models, and supporting assertions used to infer it |

## Identity, assertion, and state

The earlier time-based versioning model separated immutable identity from changing state. This foundation extends that insight:

```text
Identity → Assertions → projected state
```

State is a projection over relevant assertions under a chosen context and knowledge time. It is not necessarily a single stored object and must not erase the claims from which it was derived.

Likewise, structure, semantics, assertions, state, presentation, and execution should remain separable concerns.

## Non-destructive knowledge evolution

Corrections do not mutate an old assertion into a new truth. They create new assertions and explicit relationships such as:

- supports;
- contradicts;
- refines;
- retracts;
- supersedes;
- duplicates;
- derives-from;
- accepts or rejects within a stated community and time.

An assertion's historical record remains available even after it is rejected. Current knowledge is a projection, not an erasure of prior belief.

## Inference requirements

Every derived assertion must be explainable through:

- the supporting assertions and evidence;
- the rule, algorithm, model, or human rationale;
- the temporal scope over which the conclusion is valid;
- the context and assumptions under which it was derived;
- the confidence or uncertainty method;
- the actor or process responsible for the derivation.

Inference must be temporally closed: a conclusion cannot be treated as valid outside the compatible temporal scope of its supports.

## Implications for CTI exchange

STIX objects, MISP attributes and objects, RDF statements, reports, and database records may serve as source representations or projections. They should not be assumed to be the canonical assertion model. Import and export mappings must preserve, or explicitly disclose loss of:

- assertion identity;
- source and transformation provenance;
- confidence semantics;
- temporal axes;
- contradiction and supersession;
- community-specific acceptance.

## Challenges

- Assertion [reification](https://en.wikipedia.org/wiki/Reification_(knowledge_representation)) can create large storage and query overhead.
- Fine-grained claims can become unusable without aggregation and projection.
- Confidence values from different methods may not be comparable.
- Identity resolution must not silently collapse distinct claims or entities.
- Automated assertions can amplify errors faster than humans can review them.

## Open questions

- What is the canonical proposition model: typed relations, logical forms, frames, or a layered combination?
- What assertion granularity is useful for analysts?
- How should nested assertions and claims about claims be represented?
- How are collective belief and consensus modeled without manufacturing a single truth?
- Which truth-maintenance algorithms scale to operational volumes?
- How should uncertainty propagate across derived assertions?

## Related foundations

- [0001 — No One Ring](0001-No-One-Ring.md)
- [0003 — Temporal Substrate](0003-Temporal-Substrate.md)
- [0004 — Universe of Reality and Knowledge](0004-Universe-of-Reality-and-Knowledge.md)
- [0005 — Research Roadmap](0005-Research-Roadmap.md)
