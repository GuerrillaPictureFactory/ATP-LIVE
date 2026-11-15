# ATP TODAY — Daily Match List

A mobile-first installable ATP singles scoreboard. The front page shows only matches scheduled for the current local day, grouped by tournament and ordered live, upcoming, then finished.

## Publish with GitHub Pages

1. Upload `index.html`, `manifest.webmanifest`, `icon.svg`, and `sw.js` to the root of your existing public `atp-live` repository (replace the existing files).
2. Commit the changes.
3. GitHub Pages should redeploy automatically. If it does not, open **Settings → Pages** and confirm **Deploy from a branch**, branch `main`, folder `/(root)`.
4. Open `https://YOUR-GITHUB-USERNAME.github.io/atp-live/` and refresh the page.

## Install on iPhone

Open the published address in Safari → Share → Add to Home Screen.

## Data source

The app currently uses ESPN's public ATP scoreboard JSON endpoint:
`https://site.api.espn.com/apis/site/v2/sports/tennis/atp/scoreboard`

Flashscore does not publish an open developer API. Its terms prohibit scraping, embedding, aggregating or recreating its content without express consent. For that reason this version links directly to Flashscore rather than scraping its data. If you have an authorised Flashscore data API or licensed provider key, the app can be adapted to use it.

The ESPN endpoint is undocumented and coverage/update frequency can vary. This is an independent fan-made app, not affiliated with ATP, ESPN or Flashscore.

- Requests today's local date and filters the list to today's matches.
- Refreshes every 30 seconds while the page is visible.
- The app shell can be cached; live scores still require an internet connection.
