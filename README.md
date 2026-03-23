# mgdufour.github.io

A personal GitHub Pages site hosting links and notes.

## Live site

This site is served via GitHub Pages at
[https://mgdufour.github.io/](https://mgdufour.github.io/).

## Contents

- `index.html` — homepage with links and notes
- `commit-reverts.md` — notes and link history
- `SECURITY_CHECKLIST.md` — security baseline, scan results, and CI policy
- `reports/` — archived local Lighthouse HTML reports

## Preview locally

To preview the site locally, run a simple HTTP server from the repository root.

```powershell
py -m http.server 8000
# or
python -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in your browser.

## Contributing

Small content changes can be made via a branch + PR workflow.

```powershell
git checkout -b fix/readme
# edit files
git add .
git commit -m "Update README"
git push --set-upstream origin fix/readme
```

Pushing to `main` (repository root) will update the published site.

Security notes and latest scan results are tracked in `SECURITY_CHECKLIST.md`.

## License & Contact

This repository contains simple static pages and link notes. If you'd like changes or want to reach me, open an issue or contact the repository owner.