# swiftmind-web

Marketing site for [SwiftMind](https://github.com/kamaal4/SwiftMind) — an
offline-first iOS/iPadOS app for learning iOS concepts.

Static HTML and one stylesheet. No build step, no dependencies, no JavaScript.

## Pages

| File | Purpose |
|---|---|
| `index.html` | Landing page |
| `privacy.html` | Privacy policy (required for App Store submission) |
| `support.html` | Support page (required for App Store submission) |

## Local preview

```
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy

GitHub Pages, `main` branch, `/ (root)` folder. Pushing to `main` publishes.

## Keeping it honest

- Colours in `style.css` are ported from `SwiftMind/DesignSystem/Theme.swift`.
  If the app's palette changes, change the tokens at the top of the stylesheet.
- Category names and summaries in `index.html` are copied verbatim from
  `SwiftMind/Content/Resources/categories.json`.
- The counts in the "By the numbers" section come from the content JSON files.
  Re-check them when content ships.
- Screenshots in `assets/shots/` are 285×620 and are rendered at native size.
  Replace them with 2x/3x captures under the same filenames to sharpen them —
  no markup change needed.

## Before launch

Swap the "Coming to the App Store" `<span class="badge">` in `index.html` for a
real App Store link.
