# GEMINI.md — Project Workspace Rules

This file provides startup and workspace guidelines for Gemini/Antigravity operating in this directory.

## Core Rules
- **Collaborate First**: Ask clarifying questions before starting new major workflows or refactors.
- **Commit Before Edit**: Stage and commit files before modifying them, and commit immediately after.
- **Direct Feedback**: Be direct, precise, and concise. Do not use superlatives, fluff, or emojis.

## Global Context & Reference Boundaries
- **Global Context (`~/Documents/-context/`)**: Houses Bob's private identity, brand voice, and business principles.
- **Global Reference Library (`~/Documents/knowledge-base/`)**: Houses scraped market data, literature, and general facts. Keep strictly isolated from -context/.

## Strategy & Documentation Workspace
- **Domain**: Product & AI Strategy (Granola AI case study)
- **Format**: Markdown strategy artifacts across 6 structured modules
- **Tooling**: Standard markdown viewer, local file editor

## Session Start Protocol (MANDATORY)
At the very beginning of a new session, Gemini MUST:
1. **Read Workspace Memory**: Immediately read the local `.context/current.md` file to load active focus, decisions, status, and open items.
2. **Review Objectives**: Read `README.md` and any local documentation to stay aligned with the project.
3. **Check Session Age**: Check the `Last Session` date in `current.md`. If 2+ days have passed since the last session, ask Bob for a brief recap of what happened in between.

## Session End Protocol (MANDATORY)
When Bob signals end of session ("wrap up", "close out", "end session"):
1. Update `.context/current.md` (Active Focus, Recent Decisions, Next Steps, Open Items, dates).
2. Create session log at `.context/sessions/YYYY-MM-DD-topic.md`.
3. Update `.context/changelog.md` with file-change revert instructions.
4. Stage and commit `.context/` updates to the project Git repository.
5. Show Bob exactly what has been logged and committed.
