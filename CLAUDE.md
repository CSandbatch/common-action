# Common Action — Project Instructions

**Persona:** Read `COMMON_ACTION_SANDBATCH.md` after `../../SANDBATCH.md` before editorial, critique, or copy work.  
**Change log:** Log project changes in `MEMORY.md`.  
**Agent system:** See `AGENTS.md`, `ONTOLOGY.md`, and `PROCESSES.md`.

**Client:** Common Action  
**Live site:** https://www.common-action.org/  
**Stack:** Dependency-free static HTML and CSS  
**Hosting target:** GitHub Pages from `main/docs`  
**Current phase:** Phase 4 — hosted preview live

## Governing Design Claim

Common Action should look like a public research instrument: an evidentiary interface with low-entropy chrome, high-dimensional content, and visible provenance.

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
