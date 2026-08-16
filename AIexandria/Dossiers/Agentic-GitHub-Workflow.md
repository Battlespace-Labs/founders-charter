# Agentic GitHub Workflow

| Field | Value |
| --- | --- |
| Status | Active operating dossier |
| Established | 2026-08-16 |
| Scope | Battlespace Labs GitHub work using Patrick, Albert/Codex, GitHub Copilot, and Claude |
| Governing doctrine | [Human-Centered Knowledge Workflow](../../Governance/Doctrine/0002-Human-Centered-Knowledge-Workflow.md) |

## Purpose

Battlespace Labs uses specialized agents according to their strengths while
keeping GitHub changes reviewable, attributable, and reversible. The workflow
removes routine Git mechanics from Patrick without assigning all reasoning,
implementation, and review to one universal tool.

## Roles and routing

| Work | Preferred participant |
| --- | --- |
| Intent, architecture, cross-project reasoning, research, and synthesis | Patrick with Albert/Codex |
| Bounded repository-local implementation and GitHub-native branch/PR work | GitHub Copilot cloud agent |
| Independent analysis, critique, implementation, or review when requested | Claude |
| Automated validation | Repository tests, linters, schemas, and GitHub Actions |
| Consequential decisions and final merge authority | Patrick |

Routing is a default, not a monopoly. Task complexity, context, risk, cost, and
demonstrated performance determine the actual assignment. Prior preference or
tool longevity does not exempt any participant from reassessment.

## Human interaction model

Patrick should normally provide only:

- the desired outcome;
- important constraints or authoritative references;
- acceptance criteria when they are not evident from the discussion.

The coordinating agent converts that intent into a bounded task, selects the
appropriate worker, preserves context, and returns a draft pull request or a
clear result for review. Patrick is not expected to operate routine branch,
commit, push, or pull-request mechanics.

## Repository trust boundary

- `main` remains human-controlled; agents work through dedicated branches and
  draft pull requests.
- Copilot uses `copilot/` branches, Claude uses `claude/` branches, and other
  agents use `agent/` branches unless a repository requires another convention.
- One agent writes to a branch or worktree at a time.
- Agent-generated changes receive the same validation and review expectations
  as human-generated changes.
- Credentials are supplied only through approved provider connections or
  GitHub secrets. They never appear in repository content, prompts, comments,
  logs, or pull-request descriptions.
- Destructive operations, governing-doctrine changes, security-boundary
  changes, public releases, and merges require explicit human authority.

## GitHub Copilot integration

Repository-wide Copilot behavior is defined in
[`.github/copilot-instructions.md`](../../.github/copilot-instructions.md) and
the shared [`AGENTS.md`](../../AGENTS.md). Copilot is the default worker for a
well-bounded repository task when GitHub-native exploration, editing, testing,
branching, and draft-PR creation provide the principal advantage.

Copilot is not the default for open-ended doctrine, cross-repository
architecture, sensitive personal material, or research requiring substantial
external evidence.

## Claude integration

Claude behavior is defined in [`CLAUDE.md`](../../CLAUDE.md) and the shared
[`AGENTS.md`](../../AGENTS.md). The
[`Claude Assistant`](../../.github/workflows/claude.yml) workflow supports:

- `@claude` in an issue or pull-request discussion;
- assignment of an issue to Claude;
- the `agent:claude` issue label.

The workflow references the GitHub Actions secret
`CLAUDE_CODE_OAUTH_TOKEN`. Activation therefore requires a repository
administrator to install or authorize the official Claude GitHub integration
and create that secret. The token value must never be committed.

The integration is deliberately opt-in rather than an automatic review on
every pull request. This limits unnecessary cost and keeps agent selection tied
to the needs of the task.

## Task lifecycle

1. Capture the outcome in normal conversation or a GitHub issue.
2. Select the worker based on the routing table.
3. Supply a bounded task with constraints, references, and acceptance criteria.
4. Work on an isolated agent branch.
5. Validate the complete change.
6. Open a draft pull request describing scope, rationale, checks, and risks.
7. Request independent review when consequence or uncertainty warrants it.
8. Patrick confirms consequential decisions and controls the merge.

## Initial acceptance test

The integration is operational when:

1. Copilot completes one bounded repository task and opens a valid draft pull
   request that conforms to the shared instructions;
2. an authorized `@claude` request produces a response or proposed change
   without exposing a credential;
3. both paths preserve `main`, attribution, validation results, and Patrick's
   merge authority;
4. the process requires no routine manual Git commands from Patrick.

## Current follow-up

- Complete the one-time Claude GitHub App/OAuth-secret activation.
- Run one small, real task through each agent path.
- Review quality, latency, cost, and intervention required before expanding
  automation or upgrading subscription tiers.
