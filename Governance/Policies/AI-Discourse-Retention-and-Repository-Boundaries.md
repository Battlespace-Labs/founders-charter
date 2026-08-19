# AI Discourse Retention and Repository Boundaries

| Field | Value |
| --- | --- |
| Status | Active policy |
| Effective | 2026-08-17 |
| Scope | AI conversation exports, coding-agent sessions, attachments, normalized corpora, and repository-bound derivatives |
| Governing doctrine | [Doctrine 0003 — Preservation Precedes Interpretation](../Doctrine/0003-Preservation-Precedes-Interpretation.md) |

## Policy outcome

Full AI-service exports and raw session artifacts are retained centrally under
[Authoritative Data Residency](https://en.wikipedia.org/wiki/Data_residency)
control, but they are not stored in Git. Private repositories are collaboration
and change-control systems, not secret vaults or unrestricted personal-data
archives.

## Storage and retrieval zones

| Zone | Purpose | Permitted material | Default AI access |
| --- | --- | --- | --- |
| Raw archive | Immutable source custody | Original exports, attachments, manifests, checksums | None; deliberate recovery only |
| Restricted enclave | High-risk retained material | Health, legal, financial, identity, security, and third-party private content | Explicit authorization only |
| Normalized corpus | Searchable derivatives with provenance | Parsed conversations and cleared attachments | Policy-filtered |
| Active retrieval | Routine reasoning context | Approved `Promote`, `Cassandra`, and relevant `Working` material | Approved workflows |
| Git repositories | Durable collaborative artifacts | Minimized, cleared, repository-relevant derivatives | Repository policy |

`Ephemeral` means excluded from routine retrieval unless deliberately requested.
It does not mean deleted.

## Prohibited from Git, including private repositories

Do not commit or upload:

- complete provider exports or wholesale normalized conversation corpora;
- credentials, tokens, recovery codes, private keys, signed bearer URLs, or
  generated secret values, whether believed current or expired;
- account-profile, settings, billing, relationship, feedback, or service
  administration metadata from provider exports;
- local session stores from Codex, Claude Code, Copilot, or another agent;
- `Restricted` conversations or unredacted health, legal, financial, identity,
  location, or security records;
- unreviewed images, audio, video, archives, documents, or other attachments;
- media with uncleared embedded metadata such as
  [Exchangeable image file format](https://en.wikipedia.org/wiki/Exif) data;
- third-party private information without a documented purpose and authority;
- a checksum, locator, or metadata field when it would materially aid recovery
  of prohibited content.

Repository visibility does not change these prohibitions.

## Repository upload gate

Before repository upload, an agent or reviewer must:

1. identify the target repository, visibility, audience, and purpose;
2. establish the minimum content necessary for that purpose;
3. scan text and machine-readable fields for secrets and high-risk identifiers;
4. inspect attachments by content and embedded metadata, not extension alone;
5. segregate `Restricted` material and third-party private content;
6. create a redacted or summarized derivative rather than changing the source;
7. validate that references and logs do not reintroduce excluded values;
8. record source lineage and transformations in a non-sensitive form;
9. inspect the complete staged diff before commit;
10. require human confirmation when residual ambiguity could expose protected
    material.

Passing an automated scan is necessary but not sufficient. Scanners can miss
secrets, misclassify identifiers, and cannot determine authority or intent.

## Secret response

When a live or potentially live secret is detected:

1. stop upload and dissemination;
2. do not print, quote, hash, or copy the value into reports, issues, prompts,
   or logs;
3. identify the issuing system and rotate or revoke the secret through its
   approved control plane;
4. record a non-sensitive incident reference;
5. rescan the derivative, staging area, Git index, and relevant logs;
6. if committed, treat rotation as mandatory and repository-history repair as
   a separate destructive action requiring explicit authorization.

## Central preservation controls

The raw archive must use encryption at rest and in transit, access logging,
integrity checks, versioned manifests, and at least one independently
recoverable backup. Repository indexes may identify the existence and custody
class of a private artifact but must not disclose its content or sensitive
locator.

## Deletion

Deletion follows the recorded exception process in
[Doctrine 0003](../Doctrine/0003-Preservation-Precedes-Interpretation.md).
Classification, repository exclusion, expiry from active retrieval, and account
cancellation do not independently authorize destruction.
