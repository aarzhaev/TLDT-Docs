# TLDT Docs

Official public documentation for [TLDT](https://tldt.me), an owner-controlled career memory and AI representation system for role fit, interview preparation, and selective professional sharing.

TLDT helps people build reviewed Career Memory, check how their experience maps to real roles, prepare for interviews, and control what an AI profile can represent publicly.

- **Documentation:** https://docs.tldt.me
- **TLDT:** https://tldt.me

## Documentation scope

This repository contains documentation for:

- getting started with TLDT
- Career Memory and owner review
- importing, generating, reviewing, and publishing career evidence
- Fast Check for role fit
- interview simulation and preparation
- public profile, chat, CV, and sharing
- integrations, account, privacy, and representation boundaries

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
