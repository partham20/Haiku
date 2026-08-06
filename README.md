# Haiku

A poetry-app UI prototype — a dark, Material-3 styled front end for browsing, reading and publishing short verse.

## Screens

| Path | Screen |
|------|--------|
| `index.html` | Entry / landing |
| `home_feed/` | Main feed of poems |
| `explore_poems/` | Discovery and browse |
| `poem_view/` | Single-poem reading view |
| `profile/` | User profile |
| `verse_noir/` | Alternate dark "verse noir" theme |

Each screen is a standalone HTML page — no build step, no framework runtime.

## Stack

- **Tailwind CSS** via the browser CDN build (with the `forms` and `container-queries` plugins)
- **Material 3 design tokens** mapped into the Tailwind theme — `surface`, `surface-container-*`, `primary`, `on-surface`, `outline`, `error` and friends, tuned for a dark palette (`#0e0e0e` background, `#57f47f` primary)
- **Google Fonts** — Plus Jakarta Sans and Manrope
- **Material Symbols Outlined** for iconography

Dark mode is class-based (`<html class="dark">`) with `darkMode: "class"` in the inline Tailwind config.

## Running it

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
```

To publish, enable **GitHub Pages** on this repository (Settings → Pages → deploy from the default branch root).

## Note

Tailwind is loaded from the CDN, which is intended for prototyping. For production, install Tailwind as a build step and ship a compiled stylesheet.
