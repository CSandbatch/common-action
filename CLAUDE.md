# Common Action — Project Instructions

**Persona:** Read `COMMON_ACTION_SANDBATCH.md` after `../../SANDBATCH.md` before editorial, critique, or copy work.  
**Change log:** Log project changes in `MEMORY.md`.  
**Agent system:** See `AGENTS.md`, `ONTOLOGY.md`, and `PROCESSES.md`.

**Client:** Common Action  
**Live site:** https://www.common-action.org/  
**Stack:** Dependency-free static HTML and CSS, with a single small JS file (`docs/app.js`) for the color-scheme switcher only  
**Hosting target:** GitHub Pages from `main/docs`  
**Current phase:** Phase 4 — hosted preview live

## What This Site Is

Common Action is the **canonical institutional site** for the organization: a single-page public memorandum that presents the thesis, fields, capabilities, and protocols as a calm, document-like reading experience. It is the front door — the version a stakeholder, partner, or funder is meant to read linearly.

It has a sister site, **Common Pitch** (`../common-pitch/`), which is the *same organization, a different purpose*: an experimental, interactive "argument cabinet" where visitors assemble, share, and present source-labeled argument cards. Same facts, two postures — Common Action is the evidentiary brochure; Common Pitch is the persuasion instrument. The two share a factual source (`https://www.common-action.org/`) and, as of 2026-06-26, a color system.

## Governing Design Claim

Common Action should look like a public research instrument: an evidentiary interface with low-entropy chrome, high-dimensional content, and visible provenance.

## Color Schemes

Two named color schemes, ported from Common Pitch and switchable at runtime via `docs/app.js`:

| Scheme | Trigger | Palette |
|---|---|---|
| `ultraviolet` (default) | `:root` | Cool blue-grey paper, deep-navy ink, electric-blue accent (`#0038ff`), yellow signal (`#efff00`) |
| `suited-chili` | `html[data-theme="suited-chili"]` | Warm cream paper, dark-brown ink, chili accent (`#ff4b1f`), amber signal (`#ffd21f`) |

The header "Color change" button toggles between them; the choice persists in `localStorage` (`common-action-theme`). An inline `<head>` script applies the stored scheme before first paint to avoid a flash. `app.js` carries **only** the scheme switcher — the site is otherwise static and dependency-free.

## Source Constraints

The source site establishes:

- Thesis: “Moving the world from chaos to comprehension.”
- Focus areas: Climate, Energy, Agriculture, Supply Chain.
- Capabilities: knowledge engineering, business intelligence, graph databases, semantic web, data science, spatiotemporal analysis, physical modeling, GIS, and NLP.
- Contact: ellie@common-action.org.

Do not present proposed language as a verified program outcome. Do not manufacture institutional proof.

## Build

The production build is in `docs/`, the GitHub Pages publishing source. It requires no compilation.

```powershell
../../.venv/Scripts/python.exe -m http.server 8770 --directory docs
```
