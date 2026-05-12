# UPN Communications Site

Static HTML host for Kry/Livi internal communications pages, embedded into SharePoint via iframe.

## Current page

- **[index.html](./index.html)** — UPN Migration Hub (project ITA-1779). Embedded in SharePoint at the [UPN-Change-project-page](https://krylivi.sharepoint.com/sites/KryliviSE/SitePages/UPN-Change-project-page.aspx).

## How this works

1. Pages are plain HTML with inline CSS — no scripts, no build step, no dependencies.
2. GitHub Pages serves the repo at `https://webbhalsa.github.io/UPN-Comm-Site/`.
3. SharePoint pages embed the Pages URL via the Embed web part. The host domain (`webbhalsa.github.io`) is added to the tenant's allowed iframe sources.
4. Updates: edit the HTML, commit/push, Pages redeploys automatically within a minute.

## Repo conventions

- Keep pages self-contained (single `.html` file with inline CSS where possible).
- Brand variables defined at the top of each page in `:root { --... }` for consistency.
- Internal links (Zendesk, Teams) point to real URLs; placeholders flagged with `TODO`.
