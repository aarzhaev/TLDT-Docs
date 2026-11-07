# TLDT Docs

Official public documentation for [TLDT](https://tldt.me), an owner-controlled career memory and AI representation system for role fit, interview preparation, and selective professional sharing.

TLDT helps people build reviewed Career Memory, find relevant vacancies, check how their experience maps to real roles, prepare for interviews, and control what an AI profile can represent publicly.

- **Documentation:** https://docs.tldt.me
- **TLDT:** https://tldt.me

## Documentation scope

This repository contains documentation for:

- the first-use workflow from CV and assistant Memory import to search and preparation
- Profile, CV publication, and private Search Profile context
- Job Search, Instant Fit, saved searches, and saved vacancies
- Career Memory, Properties, drafts, generation, publication, and export
- Fast Check and Manual/Auto Simulate
- Memory Gaps, saved text or dictated answers, and Memory Loop proposal review
- Preview, public profile, Chat ratings, sessions, summaries, and saved shares
- Cal.com meetings, integrations, account, privacy, and representation boundaries

The documentation site is built with [Mintlify](https://mintlify.com).

## Local development

Install dependencies and start the local documentation server:

```bash
npm install
npm run dev
```

Validate the documentation before publishing:

```bash
npm run validate
npx --no-install mint broken-links
```

The Mintlify configuration lives in `docs.json`. Custom visual styles are defined in `style.css`, with assets in `logo/` and `images/`.

The checked-in Mintlify CLI version is pinned so local preview stays aligned with the hosted runtime. Update it deliberately and verify both themes before committing a runtime upgrade.

## MCP

Mintlify exposes a search MCP server for the documentation at:

```
https://docs.tldt.me/mcp
```

Readers can also connect from the documentation contextual menu. Local editor configuration is available in `.vscode/mcp.json`.

## Content rule

Write for a first-time user and describe current behavior only.

If a feature depends on an owner setting, published Memory, or an integration, state that explicitly. Never present a draft, suggestion, simulation, or diagnostic report as a binding decision. Keep owner control, evidence boundaries, and the distinction between private preparation and public representation explicit.

## Content maintenance

Keep existing public page paths stable when reorganizing navigation. Verify instructions against the owning TLDT UI and implementation, not strategic plans alone. The content brief is in `.mintlify/product-brief.md`; audit and verification records are in `PROJECT_PROGRESS.md`.
