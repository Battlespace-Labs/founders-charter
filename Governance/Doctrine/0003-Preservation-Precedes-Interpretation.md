# Doctrine 0003 — Preservation Precedes Interpretation

| Field | Value |
| --- | --- |
| Status | Adopted doctrine |
| Adopted | 2026-08-17 |
| Scope | Battlespace Labs and AIexandria source artifacts, discourse archives, classifications, derivatives, and deletion decisions |
| Extends | [Doctrine 0002 — Human-Centered Knowledge Workflow](0002-Human-Centered-Knowledge-Workflow.md) |
| Related | [AIexandria Foundation 0002 — Assertion-Centric Architecture](../../AIexandria/Foundations/0002-Assertion-Centric-Architecture.md); [AIexandria Foundation 0003 — Temporal Substrate](../../AIexandria/Foundations/0003-Temporal-Substrate.md) |

## Doctrine

> **Preservation precedes interpretation. Classification controls retrieval,
> promotion, and access; it does not authorize destruction. Raw artifacts
> remain immutable unless an explicit, recorded deletion decision overrides
> retention.**

Battlespace Labs preserves original evidence before assigning meaning, value,
authority, maturity, sensitivity, or expected future use. A classification is
an assertion about how an artifact should presently be handled. It is not a
license to erase the artifact from which that assertion was derived.

This doctrine protects the longitudinal record required to develop
[AIexandria](../../AIexandria/Foundations/0000-Collaboration-Language-and-Style-Guide.md),
reconstruct decision history, and extend "Our Thing" as models, methods, and
scientific understanding advance.

## Definitions

- **Raw artifact** — the unaltered source received from a person, service,
  device, export facility, repository, or other system, together with enough
  provenance to establish its origin and custody.
- **Classification** — a reviewable assertion governing current retrieval,
  promotion, access, storage, or handling.
- **Derivative** — a normalized, redacted, summarized, transformed, indexed,
  or otherwise processed representation whose lineage resolves to its source.
- **Deletion decision** — an explicit authorization to destroy stated source
  material, recorded before execution with scope, authority, rationale, time,
  and verification requirements.
- **Tombstone** — a non-sensitive record that an artifact existed and was
  intentionally removed. A tombstone must not reproduce a secret or content
  whose retention is prohibited.

## Operating consequences

1. **Capture before triage.** Acquire and integrity-check the source before
   classification, normalization, or cleansing.
2. **Raw means immutable.** Do not edit a raw artifact in place. Corrections,
   redactions, and format conversions create linked derivatives.
3. **Classification is non-destructive.** Labels such as `Promote`,
   `Cassandra`, `Working`, `Ephemeral`, and `Restricted` govern use and access;
   none independently authorizes deletion.
4. **Cold is not gone.** Material excluded from normal retrieval remains
   discoverable through controlled, deliberate recovery.
5. **Authority remains faceted.** Original evidence is authoritative for what
   was received. Adopted doctrine and decisions remain authoritative for
   current normative meaning. A raw conversation does not become policy merely
   because it is preserved.
6. **Cleansing produces derivatives.** A repository-safe copy must retain
   provenance and identify the transformations applied without changing the
   raw source.
7. **Repository boundaries are separate from retention.** An artifact may be
   retained in the authoritative private archive while being prohibited from
   every Git repository, including a private repository.
8. **Destruction requires recorded authority.** Automation may nominate a
   deletion candidate but may not execute destruction without the required
   human decision.

## Deletion authority and record

A deletion decision is consequential and requires Patrick's explicit
authorization unless a controlling legal obligation requires execution by an
authorized custodian. The decision record must state:

- stable decision identifier;
- decision maker and authority basis;
- exact artifact identities and storage locations;
- reason for deletion;
- alternatives considered, including restriction, redaction, and
  cryptographic isolation;
- systems, replicas, indexes, and derivatives within scope;
- decision, execution, and verification times;
- executor and independent verifier;
- tombstone requirements or the reason no tombstone may remain;
- known residual copies, provider-controlled copies, or limitations.

Exposure of a live or potentially live secret requires immediate revocation or
rotation. Rotation does not itself authorize destruction of unrelated source
material. When the secret's value must not be retained, the deletion decision
may authorize targeted removal while preserving a non-sensitive incident and
lineage record.

## Relationship to non-destructive knowledge evolution

[Assertion-centric architecture](../../AIexandria/Foundations/0002-Assertion-Centric-Architecture.md)
preserves rejected and superseded claims because current knowledge is a
projection over historical assertions, not an overwrite of them. This doctrine
applies the same principle to source custody: classification and interpretation
may evolve while the evidence used to reach them remains replayable.

The retained legal-erasure question in
[Foundation 0003](../../AIexandria/Foundations/0003-Temporal-Substrate.md)
is resolved operationally, though not universally: append-oriented retention
is the default, and explicit deletion authority is the exception path.

## Conformance test

The doctrine conforms when an authorized reviewer can:

1. recover the exact preserved source and verify its integrity;
2. distinguish the source from every interpretation and derivative;
3. determine which classifications govern current retrieval and access;
4. reproduce the lineage of a promoted artifact;
5. identify every destruction event and the authority under which it occurred.
