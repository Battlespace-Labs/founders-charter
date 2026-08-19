# AI Discourse Review and Cleansing Prompts

| Field | Value |
| --- | --- |
| Status | Active operating prompts |
| Established | 2026-08-17 |
| Scope | Provider exports, normalized AI discourse, coding-agent sessions, and repository-bound derivatives |
| Governing doctrine | [Doctrine 0003 — Preservation Precedes Interpretation](../../Governance/Doctrine/0003-Preservation-Precedes-Interpretation.md) |

## Use

Run these prompts in order. Each stage has a read-only default and must produce
a report without deleting, uploading, publishing, or changing the raw source.
Substitute the bracketed variables with the actual paths and identifiers.

The prompts are controls, not proof. A human remains responsible for ambiguous
sensitivity, deletion authority, and repository publication.

## Prompt 1 — Intake and chain of custody

```text
Perform a read-only intake of [SOURCE_EXPORT]. Do not extract into a Git working
tree, modify source bytes, upload content, or delete anything.

Record: provider, account/workspace label, request and acquisition times when
known, original filename, byte size, archive inventory, export schema/version,
cryptographic checksum, earliest/latest content dates, attachment counts, and
parse errors. Do not print content values that resemble credentials or personal
identifiers. Produce a manifest and identify coverage gaps.
```

## Prompt 2 — Credential and secret quarantine

```text
Scan [STAGED_SOURCE_OR_DERIVATIVE] for live or potentially live credentials,
API keys, OAuth tokens, bearer URLs, session cookies, private keys, recovery
codes, passwords, connection strings, signed URLs, and generated secrets.

Never print, quote, hash, or reproduce a matched value. Report only a stable
artifact identifier, safe locator, secret category, confidence, issuing system
when inferable, and recommended action. Distinguish user-supplied secrets from
provider-generated metadata and examples. Do not rotate, revoke, edit, upload,
or delete automatically. Mark every affected artifact BLOCKED pending human
verification and credential rotation where applicable.
```

## Prompt 3 — Privacy and restricted-content review

```text
Review [NORMALIZED_CORPUS] for health, legal, financial, identity, location,
employment-confidential, security-sensitive, and third-party private content.
Also detect direct identifiers and combinations that create re-identification
risk.

Do not reproduce protected values in the report. Assign each artifact one of:
BLOCKED, RESTRICTED-ARCHIVE-ONLY, REDACTION-CANDIDATE, or CLEARED-FOR-NAMED-
PURPOSE. State the target purpose and repository; clearance for one purpose is
not blanket publication authority. Do not change source classifications or
delete content.
```

## Prompt 4 — Attachment and embedded-metadata review

```text
Inventory every attachment referenced by [CORPUS_OR_EXPORT]. Determine actual
format from file signatures rather than extensions. Treat archives, images,
audio, video, documents, and unknown binaries as BLOCKED until reviewed.

Inspect for embedded metadata, location/device identifiers, faces, signatures,
screenshots, credentials, account data, private correspondence, and nested
files. Do not publish previews of restricted media. Recommend either EXCLUDE,
RETAIN-IN-RESTRICTED-ARCHIVE, or CREATE-MINIMIZED-DERIVATIVE. Never modify the
raw attachment.
```

## Prompt 5 — Value classification and retrieval policy

```text
Classify each conversation in [NORMALIZED_CORPUS] as Promote, Cassandra,
Working, Ephemeral, or Restricted. Treat classification as a reviewable
assertion controlling retrieval, promotion, and access—not destruction.

Preserve conversation identity, chronology, provenance, contradictions,
supersession, and project relationships. Identify mixed-topic conversations and
low-confidence classifications. Exclude Ephemeral material from default
retrieval and Restricted material from general retrieval, but do not delete or
rewrite either class.
```

## Prompt 6 — Repository-safe derivative

```text
Create the minimum repository-safe derivative required for [PURPOSE] in
[TARGET_REPOSITORY]. Work from a copy; never modify [RAW_SOURCE]. Remove or
generalize prohibited content, strip unsafe attachment metadata, and omit
account/service administration records.

Preserve non-sensitive provenance: source artifact identity, transformation
time, transformation method, reviewer, and unresolved limitations. Re-run the
secret and privacy scans against the derivative, its filenames, metadata,
links, generated logs, and complete staged diff. Do not commit or upload unless
all blocking findings are resolved and the target purpose is approved.
```

## Prompt 7 — Independent release verification

```text
Independently verify [DERIVATIVE_OR_STAGED_DIFF] against the repository boundary
policy and its stated purpose. Do not rely on the preparer's conclusions.

Confirm: minimum necessary content, no secret values, no Restricted material,
no unreviewed attachments, no unsafe metadata, valid provenance, correct
references, and no prohibited content in history or generated files. Report
PASS, FAIL, or INDETERMINATE with safe locators and required corrective actions.
Do not upload, merge, or publish.
```

## Prompt 8 — Deletion-decision preparation and execution

```text
Prepare a deletion decision for [ARTIFACTS] under Doctrine 0003. First evaluate
restriction, isolation, redaction, targeted removal, and credential rotation as
alternatives. Do not delete anything while preparing the decision.

Require explicit human authorization identifying exact artifacts, replicas,
indexes, derivatives, authority, rationale, tombstone behavior, executor, and
verification method. After authorization, execute only the stated scope, verify
every named location, record residual limitations, and never place deleted
content or secret values in the decision record.
```
