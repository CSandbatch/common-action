# MEMORY.md — durable facts, Common Action

Stable context that changes future work. Not a diary. Committed and public.

## Constants

- **Client:** Common Action. **Live source:** https://www.common-action.org/
- **Thesis:** "Moving the world from chaos to comprehension."
- **Focus areas (Workstreams):** Climate, Energy, Agriculture, Supply Chain.
- **Capabilities:** knowledge engineering, business intelligence, graph
  databases, semantic web, data science, spatiotemporal analysis, physical
  modeling, GIS, and NLP.
- **Contact:** ellie@common-action.org
- **Sister repo:** `common-pitch` (`../common-pitch/`) — same organization,
  different posture (persuasion instrument vs. this repo's evidentiary
  brochure). Shared factual source and, as of 2026-06-26, a shared color
  system.

## Invariants (locked)

- Color schemes `ultraviolet` (default) and `suited-chili`, ported from
  `common-pitch` on 2026-06-26, held in sync with it. Canonical token values
  and switcher invariants: `AGENTS.md` § Color Schemes (Locked). No changes
  without explicit user approval.
- Static, dependency-free deployment surface — `docs/` plus one JS file
  (`app.js`) carrying the scheme switcher only.

## Do not store here

- Secrets, tokens, credentials, personal data.
- Temporary task state — that belongs to the task, not this file.

## Log

- **2026-06-26** — Phases 1–3 complete: source HTML extraction, desktop/mobile
  reference captures, and content inventory (Phase 1 — Audit); evidentiary-
  interface direction, information architecture, and palette/typography system
  (Phase 2 — Design System); semantic scaffold, responsive components, content
  migration, and the metadata/accessibility layer (Phase 3 — Build). Color
  schemes ported from `common-pitch` and locked; both repos share the token
  set from this date forward.
- **2026-07-11** — Framework restructure to bring this repo into conformance
  with `FRAMEWORK-STANDARD.md`: `SKILLS.md`, `MEMORY.md` (this file), and
  `EVALS.md` created. `MEMORY.md` moves from gitignored/private to committed
  and public — it and the retired `COMMON_ACTION_SANDBATCH.md` persona file
  were both previously listed in `.gitignore`; both lines are now removed.
  Every `../../SANDBATCH.md` / `COMMON_ACTION_SANDBATCH.md` reference was
  stripped from doctrine (`AGENTS.md`, `CLAUDE.md`); the voice floor now
  carried in `AGENTS.md` replaces them, so this repo needs nothing outside
  itself to hold its voice. `CLAUDE.md` reduced to a thin `@AGENTS.md` shim;
  its prior content (persona pointer, source-fact constants, build command,
  mission framing) redistributed into `AGENTS.md`, this file, and `ONTOLOGY.md`.
- **2026-07-11** — Evaluator audit caught stale pre-port palette in `brand/design-system.md` (the original single-scheme values, superseded 2026-06-26). Palette section now defers to `AGENTS.md` § Color Schemes (Locked) as the single authoritative table; old values retired to this log: paper `#f0eee5`, paper-light `#f7f5ed`, ink `#10232d`, ink-muted `#526168`, rule `#a5aaa5`, signal `#bedb39`, vermilion `#d84b31`.
