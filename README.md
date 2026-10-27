# koa.hayyaoe.dev

Static website for **Koa**, the offline EPUB reader. This repository contains only
the public site; the app source is kept separately.

## Pages

- `/` — landing page
- `/privacy/` — privacy policy
- `/support/` — support and FAQ
- `/terms/` — terms of use
- `/404.html` — not-found page
- `/assets/` — icon and CSS

Contact: **koa@hayyaoe.dev**

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>. The site is designed to be served from the root of
`koa.hayyaoe.dev`, so root-relative asset paths work in local preview too.

## Deploy

The site deploys with GitHub Pages from `.github/workflows/pages.yml`.

1. In this repository: **Settings → Pages**.
2. Set **Build and deployment → Source** to **GitHub Actions**.
3. Set **Custom domain** to `koa.hayyaoe.dev`.
4. After DNS checks pass, enable **Enforce HTTPS**.
5. Push to `main`, or run **Deploy website** manually.

## DNS

At the DNS provider for `hayyaoe.dev`:

| Type | Name | Value |
| --- | --- | --- |
| CNAME | `koa` | `hayyaoe.github.io` |

If the provider is Cloudflare, use **DNS only** (gray cloud) initially. GitHub may ask
for a `_github-pages-challenge-hayyaoe` TXT record; add it exactly as shown in the
Pages settings.

## Email

`koa@hayyaoe.dev` is an email alias on the `hayyaoe.dev` domain, not a website
setting. Set it up with your mail provider (for example Cloudflare Email Routing) and
route it to the inbox you monitor.

## Updating the policy

1. Edit `privacy/index.html`.
2. Update the “Last updated” date.
3. Mirror the change in the app repository's `docs/PRIVACY.md`.
4. Commit and push; the workflow deploys automatically.

App Store Connect URLs:

- Privacy: https://koa.hayyaoe.dev/privacy/
- Support: https://koa.hayyaoe.dev/support/
