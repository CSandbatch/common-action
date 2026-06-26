# Common Action Design System

## Design Thesis

An evidentiary interface: low-entropy chrome, high-dimensional content. The page borrows from research memoranda, field reports, technical standards, and public records without imitating government bureaucracy.

## Palette

| Token | Value | Use |
|---|---|---|
| Paper | `#f0eee5` | Page ground |
| Paper light | `#f7f5ed` | Elevated fields |
| Ink | `#10232d` | Primary text |
| Muted ink | `#526168` | Secondary text |
| Rule | `#a5aaa5` | Dividers |
| Signal | `#bedb39` | Active/provisional markers |
| Vermilion | `#d84b31` | Exceptions and emphasis |

## Typography

No external font dependency.

- Display: Georgia with compact tracking.
- Interface and body: modern system sans.
- Metadata: system monospace.

Hierarchy is produced by grid position, rules, measure, case, and register—not by a ladder of arbitrary type sizes.

## Layout

- Maximum canvas: 1,520px.
- Twelve-column desktop grid.
- Visible rules preserve the document metaphor.
- Mobile reading order follows the DOM exactly.
- Paragraph measure is capped near 68 characters.

## Components

- `site-header`: identity, status, and anchor navigation.
- `hero`: thesis, institutional précis, and coordination-loop diagram.
- `register-section`: numbered dossier section.
- `workstream`: indexed field with a precise operational description.
- `capability-matrix`: pressure, method, and institutional-output relation.
- `protocol-grid`: public operating commitments.
- `site-footer`: direct contact, timestamp, and legal state.

## Refusals

No glass effects, rounded card colonies, decorative dashboards, stock photography, generated imagery, or motion without informational purpose.
