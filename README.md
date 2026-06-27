# Common Action

Rebuild of [common-action.org](https://www.common-action.org/) as an evidentiary interface for climate coordination and open science.

**What it is:** the canonical institutional site — a calm, document-like single-page memorandum presenting the organization's thesis, fields, capabilities, and protocols. Its sister site [Common Pitch](../common-pitch/) serves the *same organization* with a *different purpose*: an interactive argument cabinet for assembling and presenting source-labeled claims. Common Action is the brochure; Common Pitch is the persuasion instrument. They now share a color system (see below).

**Stack:** Static HTML and CSS, plus one small JS file (`docs/app.js`) for the color-scheme switcher  
**Status:** Phase 4 — GitHub Pages preview live  
**Production files:** `docs/`
**GitHub Pages:** https://csandbatch.github.io/common-action/

## Color schemes

Two runtime-switchable schemes, ported from Common Pitch:

- **`ultraviolet`** (default) — electric blue + yellow signal on cool blue-grey paper
- **`suited-chili`** — chili red + amber signal on warm cream paper

Toggle via the header "Color change" button; the choice persists in `localStorage`.

## Preview

From the workspace root:

```powershell
.venv\Scripts\python.exe -m http.server 8770 --directory projects/common-action/docs
```

Then open `http://127.0.0.1:8770/`.

## Deliverables

| Deliverable | Status |
|---|---|
| Source-site audit | Complete |
| Design system | Complete |
| Responsive production build | Complete |
| Local visual QA | Complete |
| Production deployment | Awaiting approval/access |
