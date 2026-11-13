# Trains by MP

Pick the GO trains you take and get calendar entries for them, so your commute sits next to your classes. Schedule data will come from GO Transit's free open data, used under Metrolinx's terms.

**Status:** coming soon at https://trains.marcantoniopovolo.com · [About the project](https://marcantoniopovolo.com/projects/trains.html) · Open source (MIT)

Built by [Marcantonio Povolo](https://marcantoniopovolo.com), a Computer Engineering student at Toronto Metropolitan University. I decide what it does and review and test each change; AI coding tools help write the code.

## How I'm building it

This is a product-development project, so the problem comes before the code:

1. A one-page brief: who it's for, the problem, how success is measured and what's out of scope.
2. A short survey of TMU commuters about what actually slows them down.
3. The smallest version that helps: pick a trip, get a calendar entry.

## Layout

| Path | What it is |
|---|---|
| `site/` | The website at trains.marcantoniopovolo.com: the coming-soon page (`index.html`, `style.css`), icons and favicons. `about/` and `_redirects` send the old project page to [marcantoniopovolo.com/projects/trains.html](https://marcantoniopovolo.com/projects/trains.html) |
| `worker.js` | The API: anything under `/api/` (for now `/api/status`). Everything else is served from `site/` |
| `wrangler.jsonc` | Cloudflare settings: `site/` plus `worker.js` at trains.marcantoniopovolo.com |
| `LICENSE` | MIT: free to use, change and share |
| `AGENTS.md` | Rules for AI coding tools working in this repo |

## Publishing

Pushing to GitHub saves the code. To put `site/` online at trains.marcantoniopovolo.com, run this in the repo folder:

```
npx wrangler deploy
```

## API

The app and its API share one address. The website is served from `site/`; requests under `/api/` go to `worker.js`. While the app is coming soon there is one endpoint:

```
curl https://trains.marcantoniopovolo.com/api/status
```

## Open source

This project is open source under the [MIT License](LICENSE). Fork it, change it and make your own version; just keep the license notice. Issues and pull requests are welcome.
