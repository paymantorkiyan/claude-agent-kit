# [Project Name] — Claude Context

> Read this file first. Every session. No exceptions.
> Check `.tasks/` for active work before doing anything else.

---

## Project Overview

<!-- What is this project? One paragraph. -->

---

## Stack

<!-- List your tech stack here -->
<!-- Example:
- Language: TypeScript
- Framework: Next.js
- DB: Supabase
- Styling: Tailwind + shadcn
- Testing: Vitest + Playwright
-->

---

## Directory Structure

<!-- Paste your key directories and what they contain -->
<!-- Example:
src/
├── app/          — Next.js app router pages
├── components/   — Shared UI components
└── lib/          — Utilities and DB client
-->

---

## Coding Standards

<!-- Your non-negotiables. Examples:
- TypeScript only, no `any`
- Semantic commits: feat/fix/chore/docs
- Never commit to main directly
- Tests must pass before committing
-->

---

## Architecture and code quality

- Build every change cleanly and modularly, with clear separation of concerns. Follow the patterns already in this codebase.
- Never bolt a feature on just because it was asked for. Before writing code, find where it naturally belongs.
- Warning signs it doesn't fit: duplicating logic, adding special-case flags, reaching across layers, or growing an already large file.
- If you see any of those, stop before building and tell me: what doesn't fit, the refactor you'd recommend, how big and risky it is, and a minimal fallback. Wait for my call.
- Keep refactors separate from features: refactor first as its own change, then add the feature on top.
- Don't refactor beyond what the task needs without asking.
- Leave no dead code, debug output or silent TODOs behind.

---

## Off-Limits

<!-- Files or directories Claude must never touch -->
<!-- Example:
- .env* files — never read, write, or log
- /migrations — reference only, never edit
-->

---

## Active Sprint / Current Focus

<!-- Optional: what's being worked on right now -->
<!-- Delete this section if you don't want it -->
