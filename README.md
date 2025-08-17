# Aurora Sidebar Menu (HTML + CSS)

Neon-accent, glassy **sidebar** with off-canvas drawer on mobile — pure HTML/CSS (no JS).

## Structure
```text
aurora-sidebar/
├─ index.html
└─ styles.css
```

## Quick Start
1) Put the HTML into `index.html` and the CSS into `styles.css`.  
2) Ensure this is in `<head>`:
```html
<link rel="stylesheet" href="styles.css" />
```
3) Open `index.html` in your browser.

## Features
- **CSS-only drawer:** hidden checkbox (`#aside-toggle`) + `.burger` toggles the sidebar under `860px`.
- **Submenu:** native `<details class="group">` with a styled `.submenu`.
- **Active link styling:** `.nav-link.active` gets a teal→violet gradient.
- **Design tokens:** theme via `:root` (`--t1`, `--t2`, `--text`, `--ring`, etc.).
- **Layout:** fixed sidebar (`280px`); main `.content` uses `margin-left: 280px` on desktop.

## Customize
- **Palette:** edit `--t1` (teal), `--t2` (violet), `--text`, `--muted`.
- **Glass/blur:** `--glass` and `backdrop-filter` on `.sidebar`.
- **Sidebar width:** change `.sidebar { width: 280px; }` and match `.content { margin-left: ... }`.
- **Breakpoints:** tweak `@media (max-width: 860px)` for drawer behavior.
- **Cards grid:** `.cards` → 3/2/1 columns (edit media queries).

## Accessibility
- Burger is a `<label for="aside-toggle">`; remains keyboard toggleable.
- Focus styles via `:focus-visible` and `--ring`.
- Semantic nav (`<nav>`, links) and native details/summary for Services.

## Troubleshooting
- **Burger doesn’t open?** Confirm DOM order and id/for match:  
  `input#aside-toggle` → `label[for="aside-toggle"]` → `.sidebar`.
- **Content overlaps sidebar?** Keep `.content { margin-left: 280px; }` on desktop; it resets on mobile.
- **Blur missing?** `backdrop-filter` may be unsupported—provide darker solid backgrounds as fallback.

