# Performance Canvas Background Study (Matrix Hero)

A public study project focused on **front-end performance** and **user experience**: a premium hero section with a **deferred Canvas “Matrix” background**, **CLS-safe** image handling, and accessibility-first UI.

✅ Designed to be **Lighthouse-friendly** by:
- Deferring the Canvas animation until interaction or timeout
- Respecting `prefers-reduced-motion`
- Preventing layout shifts (CLS) with fixed intrinsic image sizing / aspect-ratio
- Pausing animation when offscreen (IntersectionObserver)

---

## Demo (GitHub Pages)
After enabling GitHub Pages, your demo will be available at:
`https://<your-user>.github.io/performance-canvas-background-study/`

---

## What’s inside
- `index.html` → standalone demo (HTML + CSS + JS)
- Canvas Matrix effect optimized with:
  - Deferred initialization
  - Frame throttling
  - Offscreen pause
  - Resize handling
- Hero layout with:
  - Social bar (horizontal)
  - Glow accents
  - Glass card CTA
  - Responsive typography via `clamp()`

---

## Performance Strategy (high level)
1. **Zero TBT start**: script starts only after user interaction or after 4 seconds.
2. **Reduced motion support**: disables effect if user prefers reduced motion.
3. **Offscreen pause**: stops requestAnimationFrame when not visible.
4. **CLS prevention**: reserves space for images using explicit `width/height` and `aspect-ratio`.

---

## How to run locally
Just open `index.html` in your browser.

If you want a local server (optional):
- VSCode extension: “Live Server”
- or run:
  - Python: `python -m http.server 8080`
  - Node: `npx serve`

---

## How to publish on GitHub Pages
1. Go to **Settings → Pages**
2. **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main** / folder: **/(root)**
3. Save → wait GitHub to publish.

---

## Notes / Improvements Ideas
- Move CSS/JS into separate files (`styles.css`, `matrix.js`) for cleaner caching strategy
- Lazy-load external icon fonts and audit third-party requests
- Replace hotlinked images with local `assets/` files
- Add a “toggle effect” UI button for UX tests

---

## License
MIT — feel free to reuse in your own projects.
