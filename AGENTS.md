# Battlespace Labs Agent Instructions

These instructions apply to every AI agent working in this repository.
Tool-specific instructions may refine them but must not weaken them.

## Mission

Maintain the foundational canons, philosophy, governance, and AIexandria
knowledge architecture of Battlespace Labs. Favor clear human-facing documents
supported by rigorous machine-readable structure.

## Read before changing anything

1. [Repository overview](README.md)
2. [Human-Centered Knowledge Workflow](Governance/Doctrine/0002-Human-Centered-Knowledge-Workflow.md)
3. [Collaboration Language and Style Guide](AIexandria/Foundations/0000-Collaboration-Language-and-Style-Guide.md)
4. Any dossier, doctrine, foundation, schema, or inventory directly governing
   the requested subject

## Operating rules

- Work only within the requested scope. Surface material ambiguity instead of
  manufacturing authority or intent.
- Use a dedicated branch and propose changes through a draft pull request.
  Never push directly to `main`.
- One agent is the active writer for a branch or worktree. Other agents review
  or work on separate branches.
- Preserve existing artifacts and Git history. Do not delete, consolidate,
  supersede, adopt, or retire material without explicit human authority.
- Treat schemas and structured objects as infrastructure, not the normal human
  interface. Keep the relevant human-facing dossier coherent.
- Preserve provenance, distinctions, rejected alternatives, contradictions,
  and supersession paths. Do not flatten them into false consensus.
- Use the canonical spelling `AIexandria` and the deliberate phrase
  `"Our Thing"` exactly as defined by the style guide.
- Follow the repository's document-independent reference-linking doctrine.
- Never commit credentials, tokens, recovery codes, private keys, personal
  data, or generated secret values.
- Prefer the smallest complete change. Do not add tools, dependencies,
  workflows, or process artifacts unrelated to the task.

## Validation and handoff

Before proposing a pull request:

- inspect the complete diff;
- validate JSON and schemas when affected;
- check repository-relative Markdown links;
- run relevant tests or linters when present;
- state what changed, why, validation performed, and any unresolved risk;
- keep the pull request in draft unless Patrick explicitly requests otherwise.

Consequential changes to doctrine, authority, scope, security, privacy, or
artifact lifecycle require Patrick's explicit confirmation before merge.
