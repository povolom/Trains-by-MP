# Trains by MP

Pick the GO trains you take and get calendar entries for them, so your commute sits next to your classes in Apple Calendar. Schedule data will come from GO Transit's free open data, used under Metrolinx's terms.

**Status:** coming soon. **Page:** https://trains.marcantoniopovolo.com

Built by [Marcantonio Povolo](https://marcantoniopovolo.com), a Computer Engineering student at Toronto Metropolitan University.

## How I'm building it

This is a product-development project, so the problem comes before the code:

1. A one-page brief: who it's for, the problem, how success is measured and what's out of scope.
2. A short survey of TMU commuters about what actually slows them down.
3. The smallest version that helps, then a check on whether people keep using it.

## Layout

| Path | What it is |
|---|---|
| `site/` | What Cloudflare serves at trains.marcantoniopovolo.com: the coming-soon page (`index.html`), the project page (`about/`), shared styles (`page.css`), icons and favicon. Built by `build_app_pages.py` in my portfolio folder. |
| `wrangler.jsonc` | Cloudflare Worker settings: serve `site/` at trains.marcantoniopovolo.com. Publish with `npx wrangler deploy`. |
