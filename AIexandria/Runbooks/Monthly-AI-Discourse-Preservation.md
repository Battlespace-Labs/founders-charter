# Monthly AI Discourse Preservation Runbook

| Field | Value |
| --- | --- |
| Status | Active runbook |
| Established | 2026-08-17 |
| Owner | Patrick |
| Cadence | Monthly master cycle; session-close capture for material coding work; fourteen-day coding-session safety sweep |
| Governing policy | [AI Discourse Retention and Repository Boundaries](../../Governance/Policies/AI-Discourse-Retention-and-Repository-Boundaries.md) |

## Objective

Preserve recoverable context from ChatGPT, Claude, GitHub Copilot, Codex/Work,
Claude Code, and successor tools without treating any vendor as the
authoritative long-term record.

Monthly is the correct master cadence. It is not sufficient as the only
cadence: GitHub documents a 28-day retention period for messages in Copilot
Chat on GitHub, while Anthropic documents that local Claude Code sessions may
be retained for only up to 30 days. Material coding sessions therefore require
capture at session close, with a fourteen-day safety sweep.

## Cadence

| Trigger | Required action |
| --- | --- |
| First day of each month | Request full provider exports and reconcile the prior cycle |
| Every fourteen days | Review uncaptured Copilot, Claude Code, and Codex/Work sessions |
| End of a material coding session | Persist issue, pull request, commit, decision, and Session Continuity Object references |
| Major milestone or consequential decision | Capture immediately; do not wait for the monthly cycle |
| Before cancellation, migration, plan change, or account deletion | Request all available exports and verify custody first |

## Provider capability register

| Provider or surface | Current supported capture | Known boundary | Required BSL action |
| --- | --- | --- | --- |
| ChatGPT personal account | **Settings → Data Controls → Export Data** or the OpenAI Privacy Portal; ZIP includes chat history and other account data | OpenAI says generation can take up to seven days and the download link expires after 24 hours; Business and Enterprise exports are not available through this personal-account path | Request monthly; download promptly; retain raw ZIP outside Git; parse a derivative only after integrity capture |
| ChatGPT Work and Codex surfaces | Account export may contain conversation and asset records from these surfaces, as observed in the August 2026 BSL export | Official documentation does not guarantee complete coverage of every local or tool-specific session artifact | Treat account export as partial until verified; preserve material outputs and session handoff state at session close |
| Claude personal account | **Settings → Privacy → Export data** in the web or desktop application; export includes conversation and user data | Export cannot be initiated from mobile; email link expires after 24 hours | Request monthly and retain the raw export outside Git |
| Claude Code | Resumable local sessions and prospective structured output using supported command-line output formats | Local sessions may be retained only up to 30 days; no complete account-style bulk export is documented | Capture material session outcomes immediately; sweep within fourteen days; quarantine any copied local session store outside Git |
| GitHub personal account | **Settings → Account → Export account data** creates a `tar.gz` account archive | GitHub documents account and repository metadata, not a guarantee of complete Copilot chat transcripts | Request monthly for GitHub provenance; do not treat it as Copilot transcript backup |
| GitHub Copilot Chat on GitHub | Recent conversation history in the Copilot interface | Up to 100 recent conversations; messages are permanently deleted after 28 days; no documented bulk chat export | Persist material work into issues, pull requests, commits, and decisions at session close; perform fourteen-day sweep |
| Copilot coding agent | GitHub issues, agent branches, commits, pull requests, reviews, and audit events | Informal chat or local IDE context may not be represented completely | Treat repository-native artifacts as the durable operational record and capture missing rationale in the issue or decision artifact |

## Monthly procedure

### 1. Establish the cycle

Create a cycle identifier using `YYYY-MM` and a private staging directory that
is outside every Git working tree. Record the participating accounts,
workspaces, devices, and provider surfaces.

### 2. Request exports

Request ChatGPT, Claude, and GitHub account exports. Do not submit repeated
requests while one is pending. Record request time, account identity, provider,
and expected delivery mechanism without recording a credential.

### 3. Capture coding surfaces

For Copilot, Claude Code, and Codex/Work:

- enumerate material sessions since the last successful cycle;
- confirm that code changes live in a repository branch or pull request;
- capture decisions, constraints, open questions, and pending actions in the
  relevant issue, dossier, decision record, or Session Continuity Object;
- preserve an available vendor or local transcript only in the encrypted raw
  archive, never in Git;
- record coverage gaps explicitly.

### 4. Acquire and freeze

Download each provider export before its link expires. Do not reorganize or
edit the downloaded package. Record byte size, cryptographic checksum,
acquisition time, provider, account or workspace, and original filename in a
manifest conforming to
[`ai-export-manifest.schema.json`](../Knowledge/schemas/ai-export-manifest.schema.json).

### 5. Scan before centralized ingestion

Apply the staged prompts in
[AI Discourse Review and Cleansing Prompts](../Prompts/AI-Discourse-Review-and-Cleansing.md).
Matched secret values must never appear in the scan report. Quarantine raw
provider exports, account metadata, local session stores, and attachments from
Git regardless of scan outcome.

### 6. Preserve centrally

Place the immutable package and manifest in the encrypted authoritative archive
using this logical layout:

```text
AI-Discourse/
  provider/
    account-or-workspace/
      YYYY/
        YYYY-MM/
          raw/
          manifests/
          derivatives/
          reviews/
```

The physical platform may change. The manifest and identity must remain
portable, consistent with the composable architecture of
[AIexandria Foundation 0001 — No One Ring](../Foundations/0001-No-One-Ring.md).

### 7. Derive without mutation

Create normalized, redacted, or classified derivatives in a separate location.
Record source identity and transformations. Do not alter the raw package or
silently overwrite an earlier derivative.

### 8. Verify and close

Verify checksums after transfer, confirm at least one independently recoverable
copy, record missing surfaces and exceptions, and mark the cycle `complete`,
`partial`, or `failed`. A partial cycle remains open until its gaps are accepted
or resolved.

## Session-close minimum for coding agents

A material session is preserved when the durable record identifies:

- objective and repository;
- issue or task identifier;
- branch, commits, and pull request when applicable;
- decisions and rejected alternatives;
- validation performed;
- unresolved questions and pending actions;
- agent/model and relevant tool surface;
- links to the prior and successor Session Continuity Objects when used.

Raw terminal history is neither required nor sufficient and must not be placed
in Git merely to claim completeness.

## Verification sources

- [OpenAI data export instructions](https://help.openai.com/en/articles/7260999-how-do-i-export-my-chatgpt-history-and-data)
- [Claude data export instructions](https://support.claude.com/en/articles/9450526-export-your-claude-data)
- [GitHub personal-account archive instructions](https://docs.github.com/en/get-started/archiving-your-github-personal-account-and-public-repositories/requesting-an-archive-of-your-personal-accounts-data)
- [GitHub Copilot Chat retention](https://docs.github.com/en/copilot/how-tos/copilot-on-github/chat-with-copilot/chat-in-github)
- [Claude Code data usage and retention](https://docs.anthropic.com/en/docs/claude-code/data-usage)

Vendor behavior can change. Revalidate this capability register quarterly and
whenever a provider changes plans, interfaces, retention, or export format.
