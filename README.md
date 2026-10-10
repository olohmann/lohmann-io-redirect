# lohmann-io-redirect

Azure Static Web App (Free) that redirects `lohmann.io` and `oliver.lohmann.io` to https://github.com/olohmann.

- Redirect rules: `public/staticwebapp.config.json` (302, so it can be changed later without browser caching issues).
- Deployment: GitHub Action on push to `main` (secret `AZURE_STATIC_WEB_APPS_API_TOKEN`).
- DNS lives in Azure DNS zone `lohmann.io`; the apex is an alias record to the Static Web App, `oliver` is a CNAME.
