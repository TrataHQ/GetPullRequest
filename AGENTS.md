# Documentation project instructions

This is the Mintlify docs site for **GetPullRequest (GPR)**. Product source of truth lives in `apps/gpr` in the monorepo (not in this folder).

## Grounding rules

- Document only what exists in `apps/gpr` (backend, mobile, daemon under `deamon/`, landing install scripts).
- Prefer `apps/gpr/AGENTS.md`, `apps/gpr/task.md`, and `apps/gpr/docs/task-lifecycle-state-machine.md` over marketing copy or root `README.md`.
- Do not invent CLI commands, install paths, providers, or OAuth flows.
- Implemented enrichments today: **GitHub**, **Jira**, **Slack**. Linear is not wired. Do not document Linear, GitLab, Bitbucket, or Trello as live.
- Default execution model is **BYOA**: agents run on the user’s paired machine via the `gpr` daemon.
- Daemon package path is `apps/gpr/deamon` (spelling intentional). Binary name is `gpr`.

## Terminology

| Prefer | Avoid |
|---|---|
| workspace | project (for execution identity) |
| machine / daemon | runner, worker node (for the paired host) |
| task | ticket (unless referring to a synced GitHub/Jira/Slack item) |
| agent session | chat (when discussing ACP session lifecycle) |
| coding agent | AI model (when discussing Cursor / Claude / Codex) |

## Style preferences

- Active voice, second person ("you")
- Short sentences. One idea per sentence.
- Sentence case for headings
- No em dashes
- No filler marketing language
- Bold UI labels: open **Settings**
- Code formatting for commands, paths, env vars, and status names
- Include copy-pasteable command snippets where humans need them

## Content boundaries

- User-facing docs only. Skip internal Nx/dev workflows unless a troubleshooting step needs them.
- Do not document unfinished CLI surfaces (for example `gpr install <adapter>` is referenced in discover output but not registered).
- App Store may be pre-register only; Android is on Google Play (`com.pullrequest`).
