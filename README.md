# Deario — Website

Public marketing/support site for the **Deario** iOS app. This repo contains
**only** the static support and privacy pages — the app's source code lives in a
separate private repository.

Live pages:

- Support / home — <https://deario.app/>
- Privacy Policy — <https://deario.app/privacy>

## Structure

```
index.html          → support page + FAQ      (deario.app/)
privacy/index.html  → privacy policy          (deario.app/privacy)
CNAME               → custom domain for GitHub Pages
.nojekyll           → serve files as-is, skip Jekyll processing
```

Links between pages are **relative**, so the site also works correctly on the
default `https://<user>.github.io/deario-site/` URL before the custom domain is
attached.

## Publishing (GitHub Pages)

1. Push this repo to GitHub as a **public** repository.
2. In the repo: **Settings → Pages → Build and deployment**.
   - **Source:** Deploy from a branch
   - **Branch:** `main` / `/ (root)`
3. (Custom domain) Under **Settings → Pages → Custom domain**, enter `deario.app`,
   then add these DNS records at your domain registrar:
   - Four `A` records for the apex pointing at GitHub Pages:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - (optional) a `CNAME` record for `www` → `<user>.github.io`
4. Enable **Enforce HTTPS** once the certificate is issued.

If you are **not** using the custom domain yet, delete the `CNAME` file and the
site will be served at `https://<user>.github.io/deario-site/`.

## Contact

deario.support@gmail.com
