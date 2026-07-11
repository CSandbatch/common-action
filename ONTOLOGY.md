# Common Action — Project Ontology

Entity taxonomy for the Common Action website.

## Project

Common Action is a knowledge-infrastructure initiative focused on climate coordination and the open-science transition.

## Posture

The stance a repo's interface takes toward the same underlying facts. This repo holds the **evidentiary-brochure** posture: linear, document-like, read start to finish. `common-pitch` holds the **persuasion-instrument** posture on the same facts: interactive, assembled by the visitor. Full framing: `AGENTS.md` → Mission.

## SourceSite

The public page at `https://www.common-action.org/`, audited as the factual source for the rebuild.

## ProductionSite

The dependency-free implementation in `docs/`.

## Thesis

A concise governing proposition that orients the institution: moving the world from chaos to comprehension.

## Workstream

One of four public fields: Climate, Energy, Agriculture, or Supply Chain.

## Capability

A technical method Common Action can apply to knowledge coordination.

## Protocol

A public operating principle concerning traceability, uncertainty, interoperability, or collective work.

## ProvenanceSignal

Interface metadata that exposes status, recency, authorship, scope, or evidentiary limits.

## ColorScheme

A **locked** named palette applied through CSS custom properties and switched at runtime. The site has exactly two, ported from Common Pitch and held in sync with it: `ultraviolet` (default — electric blue + yellow signal) and `suited-chili` (chili + amber). Canonical token values and switcher invariants are defined in `AGENTS.md` → **Color Schemes (Locked)**. Adding, removing, renaming, or recoloring a scheme requires explicit user approval.

## Artifact

| Type | Path | Description |
|---|---|---|
| `production-page` | `docs/` | Deployable static website and GitHub Pages source |
| `brand-document` | `brand/` | Design tokens and visual rules |
| `audit-record` | `audit/` | Source-site evidence and findings |
| `screen` | `audit/screens/` | Visual QA captures |
