# ATP LIVE — Match Centre

A small installable progressive web app for ATP match schedules and scores.

## Publish with GitHub Pages

1. Sign in to GitHub and create a **new public repository** named `atp-live`.
2. Upload the four files in this folder (`index.html`, `manifest.webmanifest`, `icon.svg`, `sw.js`) to the repository root.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main**, folder **/(root)**, then Save.
6. Wait for GitHub Pages to publish. Your app address will be:
   `https://YOUR-GITHUB-USERNAME.github.io/atp-live/`

## Install on iPhone

1. Open the published address in Safari.
2. Tap Share → Add to Home Screen.
3. Tap Add.

## Data source

The app requests the local calendar date from ESPN's public ATP scoreboard JSON endpoint and selects the tournament with live matches, or the nearest current/upcoming tournament:
`https://site.api.espn.com/apis/site/v2/sports/tennis/atp/scoreboard`

The endpoint is undocumented and coverage/update frequency can vary. This app is a fan-made scoreboard and is not affiliated with the ATP or ESPN. The ATP Finals is identified as the season-ending championship, not a Masters 1000 event.

## Notes

- Match list refreshes every 30 seconds while the page is visible.
- The page shell can be cached for repeat visits; live scores still require a network connection.
- GitHub Pages hosts the static app. It does not proxy or guarantee the data feed.
