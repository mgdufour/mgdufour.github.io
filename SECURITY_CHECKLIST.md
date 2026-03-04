# Security Checklist

Last updated: 2026-03-04

This checklist is for this static GitHub Pages site.

## Monthly checks

- [ ] Run [SecurityHeaders.com](https://securityheaders.com/) for `https://mgdufour.github.io`
- [ ] Run [Mozilla Observatory](https://observatory.mozilla.org/) for `https://mgdufour.github.io`
- [ ] If using a custom domain, run [SSL Labs](https://www.ssllabs.com/ssltest/)
- [ ] Confirm GitHub Pages still has **Enforce HTTPS** enabled
- [ ] Confirm no secrets/private tokens are committed (`git log`, repo search, secret scanning)
- [ ] Confirm GitHub account 2FA remains enabled

## Repo settings (one-time baseline)

- [ ] Enable branch protection on `main`
- [ ] Enable Dependabot alerts
- [ ] Enable secret scanning (where available)
- [ ] Require PR reviews for sensitive changes (optional for personal workflow)

## Site code checks

- [ ] Keep `target="_blank"` links paired with `rel="noopener noreferrer"`
- [ ] Keep external dependencies minimal (prefer no third-party scripts)
- [ ] Keep Content Security Policy aligned with actual resources
- [ ] Re-run accessibility and security checks after major edits

## Current policy baseline in `index.html`

- Referrer policy set to `strict-origin-when-cross-origin`
- CSP meta policy set for static content:
  - `default-src 'self'`
  - `script-src 'none'`
  - `style-src 'self' 'unsafe-inline'`
  - `img-src 'self' https://github.com https://avatars.githubusercontent.com data:`
  - `object-src 'none'`
  - `base-uri 'self'`
  - `frame-ancestors 'none'`

## Notes

- GitHub Pages does not provide full custom response header control for user pages.
- If you need stronger header control (HSTS, full CSP at header-level, Permissions-Policy), front the site with a service like Cloudflare or move hosting to a platform with configurable headers.
