# mgdufour.github.io

A personal GitHub Pages site hosting links and notes.

## Live site

This site is served via GitHub Pages at https://mgdufour.github.io/ (published from the repository root of this `mgdufour.github.io` repository).

## Contents

- `index.html` — the homepage for the site
- `commit-reverts.md` — notes and link history
- `SECURITY_CHECKLIST.md` — security baseline, scan results, and CI policy

## Preview locally

To preview the site locally, run a simple HTTP server from the repository root. In PowerShell or CMD:

```powershell
py -m http.server 8000
# or
python -m http.server 8000
```

Then open http://localhost:8000 in your browser.

## Contributing

Small content changes can be made via branch + PR workflow. For quick edits you can:

```powershell
git checkout -b fix/readme
# edit files
git add .
git commit -m "Update README"
git push --set-upstream origin fix/readme
```

If this repository is your GitHub Pages site (username.github.io), pushing to `main` (or the repository root) will update the published site.

Security notes and latest scan results are tracked in `SECURITY_CHECKLIST.md`.

## License & Contact

This repository contains simple static pages and link notes. If you'd like changes or want to reach me, open an issue or contact the repository owner.

