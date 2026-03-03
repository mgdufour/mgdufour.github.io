# Accessibility Report — Lighthouse (summary)

Date: 2026-03-03

Report generated with Lighthouse (local): `localhost_2026-03-03_17-29-57.report.html`

Summary
-------

- Accessibility score: 100% (Lighthouse accessibility category = 1.0)
- Automated checks: no failing a11y audits detected (lang, title, skip link, image alt, link names, landmarks, contrast, etc.)

Key findings & recommendations
------------------------------

- Avatar image size: the GitHub avatar is large (≈460×460) while displayed smaller — serve a resized/responsive image or use `srcset` to reduce payload (~19 KiB savings).
- Cache TTL: avatar shows short cache lifetime; increase cache TTL or use a locally optimized image to save repeat-download bytes (~20 KiB savings).
- Keep the `Skip to content` link and the visible `:focus-visible` styles (already added).
- Respect `prefers-reduced-motion` for animations and transitions (already added).
- Consider documenting the accessibility decisions and audit steps in this repository (this file).

Files created by the audit
--------------------------

- `localhost_2026-03-03_17-29-57.report.html` — full Lighthouse HTML report (saved in repository root).

Changes applied before the audit
-------------------------------

- Added `Skip to content` link.  
- Removed `aria-hidden` from avatar wrapper so `img alt` is announced.  
- Added `.btn:focus-visible` styles.  
- Added `prefers-reduced-motion` rule to disable transforms/animations.  
- Increased muted color contrast.

How to reproduce the report locally
----------------------------------

1. Serve the site from the repository root:

```powershell
py -m http.server 8000
# or
python -m http.server 8000
```

2. Run Lighthouse (requires Node.js & npx):

```cmd
npx -y lighthouse http://localhost:8000 --chrome-flags="--headless" --output=html --output-path=reports/localhost_$(date +%F_%T).report.html --only-categories=accessibility --no-enable-error-reporting
```

Notes
-----

- The full HTML report is fairly large; I recommend keeping this markdown summary in the repo and storing the full HTML as a CI artifact or in a `reports/` folder only when you want snapshots.
- I can move the existing HTML report into `reports/` and commit that change if you want a retained snapshot.

Next steps
----------

- Resize or serve a smaller avatar image (I can generate and replace a local optimized copy).  
- Add a GitHub Action to run Lighthouse and upload reports as workflow artifacts.  
- Run an additional axe/pa11y sweep for complementary coverage.

Commit references
-----------------

- Accessibility fixes commit: `15b34f2` (accessibility: add skip link, focus styles, reduced-motion support, improve alt handling)
- Prior README commit: `69a4251` (new readme)