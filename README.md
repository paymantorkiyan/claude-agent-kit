# Claude Agent Kit

A portable orchestration system for Claude Code. Drop into any project to get structured, token-efficient multi-phase task execution.

---

## What This Is

Instead of one Claude session doing everything (reading files, writing code, running tests, committing) in one giant growing context — this splits work into specialized agents with small, focused contexts.

```
Conductor (opus)      — orchestrates, never codes
├── Explorer (haiku)  — reads files, creates plans
├── Builder (sonnet)  — writes code, runs builds
├── Reviewer (haiku)  — runs tests, verifies
└── Committer (haiku) — git only
```

State lives in `.tasks/` files on disk — not in the conversation. Every session starts fresh.

---

## Setup (any project)

### 1. Copy these files into your repo

```
your-repo/
├── CLAUDE.md                    ← fill this in (see below)
├── .claude/
│   └── agents/
│       ├── conductor.md
│       ├── explorer.md
│       ├── builder.md
│       ├── reviewer.md
│       └── committer.md
└── .tasks/                      ← created automatically, gitignore or commit
```

### 2. Fill in CLAUDE.md

Open `CLAUDE.md` and fill in the sections marked with `<!-- -->`:
- Project overview
- Tech stack
- Directory structure
- Coding standards
- Off-limits files

This is the only project-specific thing. The agents themselves are generic.

### 3. Gitignore (optional)

If you don't want `.tasks/` committed:
```
echo ".tasks/" >> .gitignore
```

If you want task history committed (useful for teams):
```
echo "!.tasks/" >> .gitignore
```

---

## Usage

In Claude Code, just describe what you want:

```
"Add a retention KPI card to the owner dashboard"
"Fix the login redirect bug"
"Refactor the intake form validation"
```

The Conductor picks it up, checks `.tasks/` for existing work, and runs the workflow — pausing at each checkpoint for your approval.

To resume an interrupted task:
```
"Continue"
```

---

## How It Saves Tokens

| Problem | Solution |
|---|---|
| Claude re-reads entire codebase every session | `CLAUDE.md` gives instant context; Explorer reads only relevant files |
| One giant session accumulates context | Each agent starts fresh; `.tasks/` is the memory |
| Opus doing grunt work | Haiku for Explorer/Reviewer/Committer, Sonnet for Builder, Opus only for orchestration |

---

## Applying to Existing Projects

Same steps — copy the files in, fill out `CLAUDE.md`. Existing code is unaffected. The system only touches `.tasks/` until you approve an implementation.

---

## File Reference

| File | Purpose |
|---|---|
| `CLAUDE.md` | Project context — the only file you customize |
| `.claude/agents/conductor.md` | Orchestrator — controls the workflow |
| `.claude/agents/explorer.md` | Research + planning |
| `.claude/agents/builder.md` | Code implementation |
| `.claude/agents/reviewer.md` | Test + verification |
| `.claude/agents/committer.md` | Git commits |
| `.tasks/[NNN]-[slug]/task.md` | Active task state |
| `.tasks/[NNN]-[slug]/plan/` | Phase plans |
