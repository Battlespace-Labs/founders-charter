# AIexandria Foundation 0003 — Temporal Substrate

| Field | Value |
|---|---|
| Status | Draft doctrine |
| Classification | Computational and logical architecture |

## Doctrine

> Temporal semantics belong in the computational substrate. Time is a primary coordinate of knowledge, not an optional timestamp convention layered onto stored objects.

UTOPIA must operate over both the history attributed to reality and the history of knowledge about reality. Native support is required because reconstructing these histories through ad hoc joins, filters, and application logic will not remain correct or economical at scale.

## Conceptual lineage and typed validity

The 2018 *Time-Based Versioning — Conceptual Overview* design is documented conceptual lineage for this foundation. It separated entity identity from immutable state snapshots, applied temporal intervals to structural and state relationships, and supported latest-state, point-in-time, and interval-history reconstruction. Foundation 0003 preserves those invariants while generalizing them into an assertion-centric, multitemporal knowledge architecture.

This acknowledgment does not adopt the earlier design's cyber-threat-intelligence ontology as universal doctrine:

- identity/state separation is a valid modeling pattern, but the substrate does not require universal `Identity Node` and `State Node` primitives;
- the earlier `From` and `To` fields describe version or system validity—when a modeled structure or state was created, revised, or deleted—not the duration of the modeled event;
- an `EOT` or "end of time" sentinel is one possible representation of an unbounded interval, not a logical requirement;
- destructive latest-only retention is permissible only in rebuildable projections or caches whose lineage resolves to retained authoritative history. The canonical knowledge substrate remains append-oriented.

Implementations must therefore type temporal validity explicitly. They must not silently map a version-validity interval onto reality time, observation time, assertion time, or another temporal axis.

## More than one time

An incident can involve distinct temporal acts:

| Temporal axis | Meaning |
|---|---|
| Reality or valid time | When the modeled phenomenon is claimed to have occurred or held |
| Observation time | When a person or sensor observed relevant evidence |
| Detection time | When an observer recognized the phenomenon's significance |
| Collection or acquisition time | When the observation entered a system or custody chain |
| Assertion time | When a claim was made |
| Publication time | When the claim was made available to others |
| Receipt time | When another party received it |
| Acceptance time | When a consumer or community adopted it |
| Revision or supersession time | When the claim was changed, replaced, or withdrawn |

These axes must be typed. They are not interchangeable fields named `timestamp`.

## Intervals, uncertainty, and precision

Temporal values may be:

- instants or intervals;
- open, closed, or unbounded;
- exact, estimated, or unknown;
- expressed at different precision or granularity;
- supported by different evidence and confidence.

Native interval semantics should include [Allen's interval algebra](https://en.wikipedia.org/wiki/Allen%27s_interval_algebra) relations such as `BEFORE`, `MEETS`, `OVERLAPS`, `DURING`, `STARTS`, and `FINISHES`, including their inverses and equality. These are logical primitives even when computed from canonical interval endpoints rather than materialized pairwise.

## Required query perspectives

At minimum, the substrate should distinguish:

1. **Current knowledge** — what the selected community believes now.
2. **Knowledge at a point** — what that community believed at a specified knowledge time.
3. **Knowledge during an interval** — how belief, evidence, and confidence evolved over a period.
4. **Current reconstruction of past reality** — what current knowledge says about a past reality interval.
5. **Historical reconstruction** — what a community at an earlier knowledge time believed about a reality interval.

The fourth and fifth queries are not equivalent and must never be silently conflated.

## Logical primacy and selective physicalization

Temporal relations are first-class in the logical model, query language, optimizer, and inference engine. Physical design may use:

- canonical interval endpoints;
- temporal indexes;
- event or assertion logs;
- snapshots and deltas;
- materialized relations or closures for justified workloads;
- partitioning by temporal and community dimensions;
- derived analytical projections.

Pairwise interval relations should ordinarily be computed or indexed rather than exhaustively stored. Materialization is a workload decision, not a logical-model compromise.

## Temporal closure of inference

Every derived assertion must receive a computed temporal scope. An inference cannot outlive or precede its compatible supports merely because a rule matched their non-temporal fields.

Temporal reasoning must account for:

- intersection and composition of supporting intervals;
- uncertainty and precision;
- conflicting temporal estimates;
- late-arriving observations;
- revision and supersession;
- the difference between reality scope and knowledge-history scope.

## Immutability and replay

The substrate should favor append-only knowledge evolution, drawing on principles also found in [event sourcing](https://en.wikipedia.org/wiki/Event_sourcing). New evidence and corrections create new assertion states and relationships rather than overwriting the path by which knowledge changed. This enables:

- reconstruction of historical belief;
- reproducible inference;
- audit and provenance;
- comparison of decisions against evidence available at decision time;
- counterfactual or retrospective analysis without hindsight substitution.

## Performance hypothesis

Native temporal operators, indexes, and query planning should make historical worldview construction materially more efficient and reliable than application-level conventions. This is a hypothesis requiring benchmarks rather than an assumed fact.

## Open questions

- Which temporal axes are universally mandatory, and which are typed extensions?
- What is the canonical representation of uncertain and imprecise intervals?
- How should clock disagreement, timezone uncertainty, and source precision be represented?
- Which temporal operations must be available to inference engines and query optimizers?
- What materializations make current and historical knowledge projections economical at very large scale?
- How are deletions, legal erasure, and correction handled in an append-oriented system?
- Can existing engines implement the logical model adequately, or is a new substrate required?

## Related foundations

- [0002 — Assertion-Centric Architecture](0002-Assertion-Centric-Architecture.md)
- [0004 — Universe of Reality and Knowledge](0004-Universe-of-Reality-and-Knowledge.md)
- [0005 — Research Roadmap](0005-Research-Roadmap.md)
