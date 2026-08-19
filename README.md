# indypestpros

Static site for **Indy Pest Pros** (indypestpros.com), deployed via Cloudflare.

## Deployment (root — do not reorganize)

These files serve the live site and are wired to Cloudflare:

- `index.html` — root holding page.
- `public/` — assets directory used by Cloudflare (`wrangler.jsonc` → `assets.directory`).
- `wrangler.jsonc` — Cloudflare Worker/Pages config.

## Page library (`pages/`)

Working collection of landing-page builds, sorted into folders by industry and
type. Open `pages/index.html` for a browsable index that links to every page.

```
pages/
├── index.html                          # browsable directory of all pages
├── roofing/
│   └── summit-roofing.html
├── lawn-care/
│   ├── greenthumb-instant-quote.html   # instant-quote estimator
│   ├── greenthumb-services.html
│   ├── summit-lawn-care-v1.html
│   └── summit-lawn-care-v2.html
├── hvac/
│   └── northside-heating-air.html
├── locksmith/
│   └── apex-locksmith-services.html
├── plumbing/
│   └── manifold-plumbing.html          # (was ManiFoldGreen.html — "Manifold Plumbing")
├── real-estate/
│   └── residential-redevelopment.html
├── templates/
│   └── generic-local-service.html      # re-skinnable template with placeholders
└── components/
    ├── agency-os-test-bench.html       # component lab / token playground
    ├── premium-sections-showcase.html  # reusable section blocks
    └── developer-hub.html
```

Every page is a self-contained single HTML file (inline styles or CDN assets).
Move or rename them as needed — none reference each other.

### Cleanup notes

- `Locksmith HTML Gemini .txt` was byte-identical to the `.html` and was removed.
- `Section Pack HTML .txt` was renamed to `premium-sections-showcase.html`.
