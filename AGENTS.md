# Common Action — Agent Doctrine

## Mission

Common Action is the canonical institutional site: a single-page public
memorandum presenting the organization's thesis, fields, capabilities, and
protocols as a calm, document-like reading experience — the front door a
stakeholder, partner, or funder reads linearly. Its sister repo, `common-pitch`
(`../common-pitch/`), is the same organization with a different posture: an
interactive argument cabinet for assembling and presenting source-labeled
claims. Same facts, two postures — this is the evidentiary brochure; Common
Pitch is the persuasion instrument. They share a factual source
(`https://www.common-action.org/`) and, as of 2026-06-26, a color system.

The governing design claim: this site should read like a public research
instrument — low-entropy chrome, high-dimensional content, visible provenance.

## Doctrine (compact)

Non-negotiables, restated here so this repo stands alone if cloned bare:

- **Never invent** partners, clients, metrics, publications, quotes, or
  outcomes. If a fact isn't sourced from the live site or `MEMORY.md`, mark it
  unsourced or leave it out.
- **Locked invariants don't move without explicit approval** — the color
  schemes and canonical token values below, and the static deployment surface.
- **Ask before the irreversible:** deploying, deleting, force operations.
- **Report faithfully.** A failing check is reported failing, with output.
  Done means verified by serving the site and looking, not assumed.

Voice floor: write plain and concrete — the strong verb, the named file, the
actual token value. Verdict first, then the reason. Name uncertainty out loud
instead of sanding it down. No corporate filler (*seamless, leverage,
streamline, elevate*), no hedging piles, no narrating the persona. (Fuller
register lives at `../VOICE.md` if this repo happens to be cloned alongside
it — this floor holds on its own either way.)

## Key Files

| File | Purpose |
|---|---|
| `docs/index.html` | Production page and GitHub Pages source |
| `docs/styles.css` | Production design system (two color schemes: `ultraviolet`, `suited-chili`) |
| `docs/app.js` | Color-scheme switcher only (site is otherwise static) |
| `brand/design-system.md` | Visual and interaction specification |
| `audit/content-inventory.md` | Source-content record |
| `audit/design-inventory.md` | Original-site design audit |
| `audit/qa.md` | Visual QA record |
| `ONTOLOGY.md` | Entity taxonomy |
| `PROCESSES.md` | Repeatable procedures |
| `SKILLS.md` | Task class → process → gate |
| `PHASE-PLAN.md` | Phase status |
| `MEMORY.md` | Durable facts and change log |

## Run / Gate

The gate for any visual or content change is the same: serve the production
build and look at it.

```powershell
python -m http.server 8770 --directory docs
```

Open `http://127.0.0.1:8770/`. Check 320 / 390 / 768 / 1440px: no horizontal
overflow, contrast holds, reading order matches document order, reduced-motion
and print rules fire. Full checklist: `audit/qa.md`.

## Color Schemes (Locked)

The site ships **exactly two** color schemes, switched at runtime via
`docs/app.js`. These are canonical. **Do not add, remove, rename, or recolor a
scheme without explicit user approval** — no palette "refreshes," no extra
themes, no token-value edits. Both schemes were ported from Common Pitch on
2026-06-26 and must stay in sync with it.

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

Switcher invariants: default is `ultraviolet`; choice persists in
`localStorage` key `common-action-theme`; an inline `<head>` bootstrap applies
the stored scheme before first paint; `meta[name=theme-color]` tracks the
active scheme (`#eef1f6` / `#f0e2cb`). `app.js` carries the switcher **only**
— no other client behavior.

## Routing

- `docs/` — the production build. See `docs/AGENTS.md`.
- `brand/` — the design-system spec. See `brand/AGENTS.md`.
- `audit/` — source-site evidence and the QA record. See `audit/AGENTS.md`.

## Project Rules

- Avoid SaaS cards, mesh gradients, synthetic imagery, and generic AI
  futurism.
- Maintain WCAG-oriented contrast, keyboard navigation, and reduced-motion
  compatibility.
- Treat provenance, uncertainty, and update state as interface elements, not
  afterthoughts.
- Log every material change in `MEMORY.md`.
