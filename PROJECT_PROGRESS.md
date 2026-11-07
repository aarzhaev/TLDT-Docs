# Documentation progress

## 2026-11-07: Update public docs for the current career workflow

Updated the 19 existing public pages and added seven guides, for 26 pages in
navigation. Preserved every existing public page path, the Almond theme, CSS,
logos, images, and the pinned Mintlify runtime. Only the documentation repository
changed; the application and its UI specifications were not edited.

The opening pages now show the complete path: sign in, add a CV, import useful
ChatGPT/Claude context, review and publish Memory, prepare Search Profile,
search and screen vacancies, run Fast Check and Simulate, answer Memory Gaps,
review proposed improvements, publish, and optionally share the twin with
Cal.com scheduling.

### Audit and corrections

| Area | Previous gap or outdated statement | Updated public guidance | Owning TLDT evidence |
| --- | --- | --- | --- |
| CV and Search Profile | No dedicated user guide | Upload/review/Save CV, existing-CV replacement, source selection, update and stale-profile behavior | `apps/web/app/admin/profile/ProfileWorkspace.tsx`, `apps/web/lib/career-profile/` |
| Job discovery | No coverage | Search filters, saved searches, bookmarks, recent history, stable vacancy copies, Instant Fit list/detail labels and preparation handoffs | `apps/web/app/admin/jobs/`, `apps/web/lib/jobs/` |
| Memory Gaps | No actionable answer workflow | Analysis sources, historical evidence, autosave, microphone transcription, Manual answer reuse, conflicts and manual status changes | `apps/web/components/memory-loop/gap-answer-editor.tsx`, `apps/web/lib/memory-gaps/`, `docs/memory-layer.md` |
| Memory Loop | FAQ said structured Memory extraction was unavailable | Selected saved answers, Private Raw evidence, review cards, edits and Properties refresh, new/update/private-update acceptance, separate publication | `apps/web/components/memory-loop/`, `apps/web/lib/memory-loop/`, `packages/memory/src/memory-loop.ts` |
| Import and publication | Import destination and activation instructions lagged behavior | Import Guide uploads to Derived; Memory Publish creates and activates a version; Public link remains a separate choice | `apps/web/app/admin/memory/ImportGuide.tsx`, `MemoryDashboard.tsx`, `apps/web/lib/career-profile/cv-publication.ts` |
| Memory export | Export was missing from the user workflow | Complete draft/version ZIP, Properties manifest, Private-file caution, account-export and ZIP-restoration limits | `apps/web/lib/memory-workspace-export.ts`, Memory export route and dashboard |
| Public representation and review | Profile controls, feedback and provenance guidance lagged the UI | Public settings in Profile, reply ratings, current labels, session-summary regeneration, Markdown export and separate shares | `apps/web/components/admin/profile-settings/`, `apps/web/components/chat/`, `apps/web/app/admin/AdminDashboard.tsx` |
| Meetings and integrations | No complete scheduling guide | Cal.com connection, enabled switch, duration and slot confirmation, separate external calendar link, hosted/BYOK and speech limits | `apps/web/components/admin/profile-settings/PublicLinkDashboard.tsx`, `apps/web/lib/calcom.ts`, `docs/integrations.md` |

Positioning was checked against the owner-supplied conversation and the current
`docs/product-truth/` collection. Strategic future capabilities were kept out of
released feature instructions. The application checkout inspected was
`79106daa83d1edc7f8ac55cd9c4c9c59aeb08f85`.

### Verification and scope

- Mintlify build validation passed using the pinned CLI.
- Internal-link and anchor checks passed; all 26 public pages have navigation entries and
  unique titles/descriptions, with no missing destinations.
- HTTP smoke returned 200 and the expected page title for all 26 local routes.
- Local browser review covered the quickstart, full navigation, Memory Loop,
  and the Memory Gap answer instructions. Steps, links and action tables rendered.
- The gap-answer description was checked against autosave, transcription append,
  Manual-answer import, conflict handling and generation guards in current code.
- No live paid generation, microphone transcription, booking or account mutation
  was performed. Product behavior is documented from source; this change is not
  a new end-to-end acceptance test of the application.
- Staging and application Preview/Production were not modified. The owner
  explicitly authorized publishing these docs by pushing `main`; the configured
  Mintlify source is `aarzhaev/tldt-docs`, branch `main`, at `docs.tldt.me`.

`README.md`, this record and `.mintlify/` are excluded from the hosted help site
through `.mintignore`.
