# Deario — Website

Public marketing/support site for the **Deario** iOS app. This repo contains
**only** the static support and privacy pages — the app's source code lives in a
separate private repository.

Live pages:

- Support / home — <https://kds2k2.github.io/deario-web/>
- Privacy Policy — <https://kds2k2.github.io/deario-web/privacy/>

## Structure

```
index.html          → support page + FAQ   (/)
privacy/index.html  → privacy policy        (/privacy/)
.nojekyll           → serve files as-is, skip Jekyll processing
```

Links between pages are **relative**, so they work both on the default
`github.io` URL and on a custom domain if one is added later.

## Publishing (GitHub Pages)

Already enabled: **Settings → Pages → Deploy from a branch → `main` / `/ (root)`**.
Pushing to `main` redeploys automatically within a minute or two.

## Optional: custom domain later

To move to a domain like `deario.app`:

1. Add a `CNAME` file containing the domain (e.g. `deario.app`).
2. Add four apex `A` records at your registrar pointing to GitHub Pages:
   `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
3. Set the domain under **Settings → Pages → Custom domain** and tick
   **Enforce HTTPS**.

Then update `privacyPolicyURL` in the app's `SettingsViewModel` to match.

## Contact

deario.support@gmail.com
