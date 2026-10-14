# AGENTS.md

Guidance for AI coding agents working in this repository. See `README.md` for what the project is.

## Workflow

- Every piece of work maps to a GitHub issue. Read the issue (`gh issue view <N>`) before starting, and stay within its scope. If something outside the issue needs doing, note it rather than doing it.
- Reference the issue in every commit message: `Refs #N`. The commit that completes the issue uses `Closes #N`.
- Make small, focused commits on `main` and push them.
- When a step needs a human (taking a course, creating accounts or API keys, confirming a choice), stop and ask instead of guessing.
- Notes record what Terence learned. Don't write course takeaways on Terence's behalf; help organise, explain or check them when asked.

## This repo is public

- Never commit secrets: API keys, tokens, `.env` files. Keep them in git-ignored files (e.g. `.env`, `secrets/`).
- Don't put personal or company-confidential information in code, commits, issues or notes: no employer-internal documents, processes, tools or links, no client names.
- Don't copy course material verbatim. Summarise in your own words and link to the source.
- Before committing, check `git diff --staged` for anything that looks like a credential or confidential detail.

## Environment

- macOS on Apple Silicon (arm64).
- The host's Python is old. Run Python experiments with Python 3.12+ (e.g. via `uv`) or in a container; don't depend on the host interpreter.

## Conventions

- **Layout:** `courses/<course>/notes.md` for notes; `experiments/<name>/` for runnable code, each with a README saying what it shows and how to run it.
- **Reproducible:** each experiment runs with a documented command (`make` target or script). No undocumented one-off commands.
- **Config:** read API keys and model IDs from environment variables. Don't hardcode them.
- **Check current docs:** use the official Anthropic and Claude Code documentation rather than memory. Models and features change quickly.
