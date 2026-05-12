# UPN Communications Site

Static HTML host for Kry/Livi internal communications around the UPN migration (project ITA-1779). Deployed to Azure Static Web Apps, embedded into the SharePoint UPN-Change-project-page via iframe.

**Production URL:** https://ambitious-desert-0c2ef4203.7.azurestaticapps.net
**SharePoint embed:** https://krylivi.sharepoint.com/sites/KryliviSE/SitePages/UPN-Change-project-page.aspx

## Structure

```
.
├── index.html                  Language picker (root entry point)
├── staticwebapp.config.json    CSP for iframe embed, cache headers, 404 fallback
├── CONTENT.md                  Translation source-of-truth (EN / SV / NO)
├── assets/
│   ├── css/site.css            Shared stylesheet for all hub pages
│   └── img/login/              Login screenshots extracted from Signout PDF
└── en/, sv/, no/
    ├── index.html              Main hub page per language
    └── login-guide.html        Step-by-step with screenshots, print-friendly
```

EN is the source of truth. SV and NO mirror EN structurally (identical DOM, only text content differs) — translation status in [CONTENT.md](./CONTENT.md).

## How it works

1. User lands on the root URL — sees the language picker.
2. Picks a language → choice persisted to `localStorage.upn-hub-lang` → redirects to `/en/`, `/sv/`, or `/no/`.
3. On return visits, root redirects automatically without showing the picker.
4. Each language has its own hub page (compressed: hero / timeline / steps / app impact / FAQ / support) plus an optional deeper login guide page with screenshots.
5. Top-right toggle on every page swaps languages while keeping you on the same equivalent page.

No JavaScript framework, no build step, no external CDN-loaded assets. Pure HTML + shared CSS. The only JS is ~10 lines for the language-picker persistence.

## Deploy

Local working tree → SWA production:

```bash
cd "$(dirname "$0")"
swa deploy . --deployment-token "$(az staticwebapp secrets list \
  --name upn-comm-site \
  --resource-group rg-upn-comm-site \
  --query 'properties.apiKey' -o tsv)" \
  --env production
```

To deploy to a preview environment instead, swap `--env production` for `--env preview` (or any environment name) — Azure creates a separate URL.

Prerequisites:
- `az login` to KRY-IT subscription (one-time)
- `swa` CLI installed (`npm install -g @azure/static-web-apps-cli`)

## Local preview

`file://` paths don't resolve consistently for the language redirect or shared CSS. Run a local HTTP server instead:

```bash
python3 -m http.server 8000
# then open http://localhost:8000/
```

## Updating content

- **Tweaking copy:** edit the relevant `/en/*.html`, then `/sv/*.html`, then `/no/*.html`. Keep DOM structure identical across languages. Sync any string changes back into `CONTENT.md`.
- **Adding a new screenshot:** drop the PNG into `/assets/img/login/`, reference relatively as `../assets/img/login/your-file.png` from a language sub-page.
- **Adding a new external link:** use `target="_top"` so it escapes the SharePoint iframe correctly. Update the `frame-ancestors` CSP in `staticwebapp.config.json` if the destination needs allow-listing.
- **Adding a new language:** copy `/en/` to `/xx/`, swap `lang` attrs, run translation pass, add `/xx/` link to root `index.html` lang-grid, mention it in `CONTENT.md` and this README.

## Git workflow

The `webbhalsa/UPN-Comm-Site` repo has an org ruleset requiring all changes go via pull request. The `swa deploy` command reads from the local working tree and is independent of git state — you can deploy without pushing, but commit/PR-merge for the canonical source of truth.

## Repo conventions

- HTML files use 2-space indent.
- CSS variables defined once in `assets/css/site.css` `:root`. Don't override per-file.
- No emojis in code identifiers or filenames; emojis in content text are fine (✓, ⚠, 🇸🇪, 🇳🇴, etc.).
- Internal links use relative paths (`./`, `../`). External links use full `https://` URLs.
- Translation placeholders use `_TODO_` in `CONTENT.md`.
