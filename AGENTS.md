# Common Action — Agent Doctrine

Self-contained agent system for the Common Action website project.

## Session Start Checklist

1. Read this file.
2. Read `CLAUDE.md`.
3. Read the last 30 lines of `MEMORY.md`.
4. Confirm the current phase in `PHASE-PLAN.md`.
5. Read `../../SANDBATCH.md` and `COMMON_ACTION_SANDBATCH.md` before editorial or critique work.

## Project Context

**Client:** Common Action  
**Live site:** https://www.common-action.org/  
**Current phase:** Phase 4 — GitHub Pages preview live  
**Gate:** Stakeholder approval and optional custom-domain cutover

## Key Files

| File | Purpose |
|---|---|
| `docs/index.html` | Production page and GitHub Pages source |
| `docs/styles.css` | Production design system (two color schemes: `ultraviolet`, `suited-chili`) |
| `docs/app.js` | Color-scheme switcher only (site is otherwise static) |
| `brand/design-system.md` | Visual and interaction specification |
| `audit/content-inventory.md` | Source-content record |
| `audit/design-inventory.md` | Original-site design audit |
| `PHASE-PLAN.md` | Phase status |
| `MEMORY.md` | Chronological change log |

## Local Preview

From the workspace root:

```powershell
.venv\Scripts\python.exe -m http.server 8770 --directory projects/common-action/docs
```

Open `http://127.0.0.1:8770/`.

## Color Schemes (Locked)

The site ships **exactly two** color schemes, switched at runtime via `docs/app.js`. These are canonical. **Do not add, remove, rename, or recolor a scheme without explicit user approval** — no palette "refreshes," no extra themes, no token-value edits. Both schemes were ported from Common Pitch on 2026-06-26 and must stay in sync with it.

**Scheme A — `ultraviolet`** (default, defined on `:root`):

| Token | Value | | Token | Value |
|---|---|---|---|---|
| `--paper` | `#eef1f6` | | `--rule` | `#8ea0f0` |
| `--paper-light` | `#fcfff6` | | `--rule-dark` | `#5e72c9` |
| `--ink` | `#061449` | | `--signal` | `#efff00` |
| `--ink-muted` | `#465685` | | `--vermilion` | `#0038ff` |
| `--grid-line` | `rgb(0 56 255 / 0.08)` | | | |

**Scheme B — `suited-chili`** (defined on `html[data-theme="suited-chili"]`):

| Token | Value | | Token | Value |
|---|---|---|---|---|
| `--paper` | `#f0e2cb` | | `--rule` | `#d8795f` |
| `--paper-light` | `#fff5e6` | | `--rule-dark` | `#b44732` |
| `--ink` | `#2c0d08` | | `--signal` | `#ffd21f` |
| `--ink-muted` | `#75463b` | | `--vermilion` | `#ff4b1f` |
| `--grid-line` | `rgb(104 20 12 / 0.1)` | | | |

Switcher invariants: default is `ultraviolet`; choice persists in `localStorage` key `common-action-theme`; an inline `<head>` bootstrap applies the stored scheme before first paint; `meta[name=theme-color]` tracks the active scheme (`#eef1f6` / `#f0e2cb`). `app.js` carries the switcher **only** — no other client behavior.

## Project Rules

- Color schemes are locked — see **Color Schemes (Locked)** above. Changes require explicit user approval.
- Preserve the small, static deployment surface.
- Do not invent partners, clients, metrics, publications, or project outcomes.
- Treat provenance, uncertainty, and update state as interface elements.
- Avoid SaaS cards, mesh gradients, synthetic imagery, and generic AI futurism.
- Maintain WCAG-oriented contrast, keyboard navigation, and reduced-motion compatibility.
- Log every material change in `MEMORY.md`.
