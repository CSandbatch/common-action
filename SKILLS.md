# SKILLS.md — task class → process → gate

Route the request to a process in `PROCESSES.md`, run it, then prove it. Every
task class below ends the same way: serve `docs/` on port 8770 and look at the
actual render. "Looks right" is not the gate — the served page is.

## Skill: Copy or content edit

**Trigger:** a change to text, claims, contact info, or workstream/capability
descriptions.

**Process:** Evidentiary Interface Design (steps 3–5).

**Gate:** serve `docs/` on 8770; check the changed section against `MEMORY.md`
→ Constants (thesis quote, focus areas, capabilities, contact) and confirm
nothing invented crept in. Log the change in `MEMORY.md`.

## Skill: Layout / CSS change

**Trigger:** spacing, breakpoints, or typography changes that don't touch a
color token.

**Process:** Static Build, then Visual QA.

**Gate:** serve `docs/` on 8770; check 320 / 390 / 768 / 1440px per
`audit/qa.md`'s viewport table — no horizontal overflow, contrast and reading
order intact.

## Skill: Color-scheme work

**Trigger:** anything touching `--paper`, `--ink`, `--rule`, `--signal`,
`--vermilion`, or a scheme name.

**Process:** none — this is a stop, not a task. The schemes are locked (see
`AGENTS.md` § Color Schemes). Get explicit user approval before touching
anything, and say up front that a change desyncs `common-pitch`, which shares
the same tokens.

**Gate:** no diff ships until approval is recorded in `MEMORY.md`.

## Skill: Source audit refresh

**Trigger:** the live `common-action.org` site changes and the `audit/`
record goes stale.

**Process:** Source Site Audit.

**Gate:** `audit/content-inventory.md` and `audit/design-inventory.md`
updated; new captures in `audit/screens/`.

## Skill: Visual QA pass

**Trigger:** any change above, or a standalone QA request.

**Process:** Visual QA.

**Gate:** serve `docs/` on 8770; capture desktop and mobile; record the result
in `audit/qa.md` in the same format as its existing entries.

## Skill: Launch / deploy prep

**Trigger:** a request to ship to production or check launch readiness.

**Process:** Launch.

**Gate:** `PHASE-PLAN.md` shows the outstanding task closed; stakeholder
approval confirmed before the deploy step runs — not after.
