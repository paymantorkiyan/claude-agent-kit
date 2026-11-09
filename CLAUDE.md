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

## Design system

- Before starting a new UI build, check which kind of project it is and use the matching design system:
  - Apps and software (dashboards, internal tools, logged-in screens): Meta's Astryx (https://github.com/meta/astryx). It needs React 19+ and is still in beta, so confirm with me before moving an existing live app to it.
  - Marketing sites where the look sells: the Impeccable design skill.
- If the project already has its own design system or brand tokens, follow those and ask before switching.

## Generated video and images (Higgsfield)

- Before sending anything to Higgsfield (a video, image or any generation job), make a storyboard first: each shot or scene, what's on screen, motion, text or voiceover, length, and the prompt you plan to send.
- Show me the storyboard and wait for my yes before sending, so no credits are spent on shots I haven't seen.

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
