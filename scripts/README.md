# Scripts

Optional utility scripts for the four-challenge Agentic SDLC workshop.

## `seed-backlog.sh` / `seed-backlog.ps1` — Seed the Challenge 3 backlog

These scripts create the [Challenge 3 backlog](../assets/backlog.md) as real **GitHub Issues** in a
repo, so teams pick from a real, prioritised, labelled list instead of inventing a backlog. The seeded
issues are also what an MCP server can pull as **real backlog context** in the Challenge 3 optional stretch.

Both scripts do the same thing — use the `.sh` on macOS/Linux and the `.ps1` on Windows.

### What they do

- Ensure the labels `backlog`, `priority:high`, `priority:medium`, and `priority:low` exist (created if
  missing; existing labels are tolerated).
- Create one issue per backlog item, with a title, a body derived from `assets/backlog.md`
  (description + acceptance criteria + affected layers), and the `backlog` + priority labels.
- Skip any item whose title already matches an **open** issue, so the scripts are safe to re-run.
- Print a summary of labels ensured, issues created, and issues skipped.

By default **8 issues** are seeded — one per item in `assets/backlog.md`. To change the set, edit the
backlog items in the script (and keep it in sync with `assets/backlog.md`).

### Prerequisites

- **GitHub CLI** installed — https://cli.github.com/
- **Authenticated** with `repo` scope — `gh auth login`

If `gh` is missing or unauthenticated, the scripts stop with a clear, actionable message before making
any changes.

### Usage

**Bash (macOS / Linux):**

```bash
# Seed the current repo (the one gh resolves for this directory)
./scripts/seed-backlog.sh

# Target a specific repository
./scripts/seed-backlog.sh --repo octo-org/team-1

# Preview only — prints what would be created, no API calls
./scripts/seed-backlog.sh --dry-run
```

**PowerShell (Windows):**

```powershell
# Seed the current repo
./scripts/seed-backlog.ps1

# Target a specific repository
./scripts/seed-backlog.ps1 -Repo octo-org/team-1

# Preview only — no API calls
./scripts/seed-backlog.ps1 -DryRun
```

> On macOS/Linux you may need to make the script executable first: `chmod +x scripts/seed-backlog.sh`.

### When to run it

- **Before Challenge 3, if you want real GitHub Issues.** The Markdown backlog is already sufficient
  for the workshop, so this is optional.
- Do a `--dry-run` first to confirm the target repository and see the list before creating anything.
- It is safe to re-run if items are missed or added later — duplicates are skipped by title.
