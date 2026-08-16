# GitHub Copilot instructions

Follow the repository-wide rules in [`AGENTS.md`](../AGENTS.md).

This is primarily a governance and knowledge-architecture repository. Treat its
Markdown as controlled human-facing content, not disposable prose. Treat JSON
schemas, objects, and inventories as supporting machine infrastructure.

When assigned a task:

1. Read the governing doctrine and the existing artifact before proposing a
   change.
2. Work from the selected base branch on a `copilot/` branch.
3. Make the smallest complete patch that satisfies the stated acceptance
   criteria.
4. Preserve document lineage, relative links, canonical vocabulary, and the
   distinction between adopted doctrine and working material.
5. Validate affected Markdown links and structured files.
6. Open or maintain a draft pull request with a concise explanation of scope,
   rationale, validation, and unresolved questions.

Do not infer adoption, rewrite governing meaning, merge the pull request, push
to `main`, expose credentials, or expand the task into adjacent BSL projects.
Escalate unresolved authority or meaning to Patrick in the pull request.
