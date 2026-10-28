# WorkChamp website

Marketing site for WorkChamp. AI enablement for marketing agencies and in-house marketing teams.

## Pages

| File | Role | Nav label |
|---|---|---|
| `index.html` | Homepage, both service lines and both audiences | Home |
| `ai-workflows.html` | Service page, AI operations and enablement | AI operations |
| `seo-ai-search.html` | Service page, organic plus AI visibility | SEO & AI search |
| `agencies.html` | Audience page, agencies | For agencies |

Every page ends in the same `#book` discovery call form.

## How these files are built

Each page is a single self-contained HTML file. CSS is inline in a `<style>` block, images are base64 data URIs, and the only external resource is Google Fonts. There is no build step, no framework and no dependencies. Open any file in a browser and it works.

This is deliberate. It keeps each page portable and lets the whole site be previewed as one document. The cost is that files are large and single-line, so diffs are not human readable. Review rendered pages, not diffs.

Source images live in `assets/` for reference. The copies the pages actually use are embedded.

## Design system

- Typeface: Montserrat
- Navy `#0F2340`
- Signal Orange `#FF7A59`
- Cyan `#06B6D4`
- Light gray `#F2F4F7`

Section rhythm alternates navy, tinted band and white. No two dark sections sit next to each other. Navy sections carry a dot-field texture and an orange bloom.

## Copy rules

Enforced across every page.

- No em dashes anywhere
- No emojis
- No "it's not X, it's Y" construction
- No agency speak and no AI hype
- Sentence case headlines, second person, Canadian spelling
- Every statistic carries its source in visible text
- No invented client results or case studies

Full brief in `docs/copy-brief.md`.

## Hosting

Served by GitHub Pages from the default branch root. `.nojekyll` is present so Pages serves files as-is.

## Open items

- The lead form posts to `PASTE_YOUR_APPS_SCRIPT_URL_HERE`. Until that endpoint is deployed the form shows its success state and sends nothing.
- `quiz.html`, the AI Readiness Assessment, is linked from two pages and has not been built. Spec is in the WorkChamp project docs.
- No custom domain, favicon, OG cards, analytics or sitemap yet.
- Pricing is not stated anywhere on the site.
