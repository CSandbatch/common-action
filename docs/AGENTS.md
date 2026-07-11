# docs/ — production build

The deployable static site and GitHub Pages source: `index.html`,
`styles.css`, `app.js`. This is what ships to https://www.common-action.org/.

## Local rules

- `app.js` carries the color-scheme switcher only — no other client
  behavior.
- Color tokens in `styles.css` are locked; see `../AGENTS.md` § Color Schemes
  (Locked). No token edits without explicit approval.
- Semantic HTML, dependency-free CSS. No build step, no external requests.

## Gate

```powershell
python -m http.server 8770 --directory docs
```

Open `http://127.0.0.1:8770/`. Check 320 / 390 / 768 / 1440px: no horizontal
overflow, contrast holds, reading order matches document order, reduced-motion
and print rules fire.

## Gotchas

- The header "Color change" button toggles `data-theme`; the choice persists
  in `localStorage['common-action-theme']`. An inline `<head>` script applies
  it before first paint — removing that reintroduces a flash.
- `meta[name=theme-color]` must track the active scheme's `--paper` value.

Project doctrine: `../AGENTS.md`.
