# GainTrace docs

Public documentation for the [GainTrace](https://gaintrace.com) API, built with [Mintlify](https://mintlify.com).

## Structure

- `docs.json` — site config (navigation, theme, branding)
- `openapi.json` — OpenAPI 3.1 spec; the **API reference** tab is auto-generated from it. Keep it in sync with the `/api/v1/*` handlers in `gaintrace-app`.
- `index.mdx`, `quickstart.mdx`, `authentication.mdx` — guide pages
- `logo/`, `favicon.svg` — brand assets

## Local development

The Mintlify CLI needs an LTS Node version (it refuses Node 25+):

```bash
nvm use 20
npm i -g mint
mint dev            # preview at http://localhost:3000
mint broken-links   # validate internal links
```

Validate the OpenAPI spec on any Node version:

```bash
npx @redocly/cli@latest lint openapi.json
```

## Deployment

Mintlify deploys automatically on every push to the connected branch.
