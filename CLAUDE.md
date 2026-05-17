# CLAUDE.md — BSJ Tools

> For full global rules, see ~/.claude/CLAUDE.md. This file contains project-specific overrides and context.

---

## Project Identity

- **Name:** BSJ Standalone HTML Tools
- **Type:** Collection of standalone, single-file HTML tools for BSJ staff and students
- **Users:** BSJ teachers and students (British School Jakarta, internal use only)
- **Deployment:** None — tools run locally by opening the file directly in a browser
- **Repository:** https://github.com/TMetters/bsj-tools

## Tech Stack

- Standalone HTML (HTML + CSS + JavaScript in a single `.html` file per tool)
- No build step, no framework, no dependencies
- Must run by opening the file directly in a browser — no server required
- AI backend (where applicable): Anthropic Claude API (claude-sonnet-4-6)
- API keys: entered by the user via a UI input field at runtime — never stored in any file

## BSJ Branding (Apply to All Tools)

- Primary font: Montserrat (Google Fonts)
- Navy: `#0d2240`
- Blue: `#0099d6`
- Red: `#cc0011`
- White: `#ffffff`
- Tone: Professional, clean, institutional
- Do NOT use purple gradients, Inter, Roboto, or generic AI aesthetics

## Core Rules (Every Session)

1. Always read a file fully before editing it
2. Never rewrite whole files — make targeted edits only
3. After every edit, run: `git diff` to show exactly what changed
4. After every edit, run: `git add . && git commit -m "auto: [describe change]"`
5. Never use `cp` to overwrite a file — always edit in place
6. Check for broken paths, missing tags, and syntax errors after every change
7. If unsure about a path or filename, list the directory first before acting

## Branch Rules

- Always work on the `agent-work` branch (current: `agent-work-20260517`)
- Never commit to `main`
- Thomas reviews and merges

## Security Rules

- Never read, print, or `cat` any `.env` file under any circumstances
- Never hardcode API keys in any HTML file — users paste keys into a UI field at runtime
- No secrets, tokens, or credentials should ever appear in any committed file

## Autonomous Operation

- Work through tasks without asking for confirmation
- Make sensible decisions and keep moving
- Only stop if genuinely blocked on ambiguous project-specific details
