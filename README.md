# Michigan Old-Growth Forests Map

An interactive map of the 27 Michigan forests in the
[Old-Growth Forest Network](https://www.oldgrowthforest.net/michigan).

Built with [Leaflet](https://leafletjs.com/) + OpenStreetMap tiles. It's a single
static `index.html` — no build step, no server, no API keys. All forest data is
inlined into the page.

## View it locally

Just open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server
# then visit http://localhost:8000
```

## Host it free on GitHub Pages

1. Create a repo and push these files:
   ```sh
   git init && git add . && git commit -m "Michigan old-growth forests map"
   git branch -M main
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
2. In the repo: **Settings → Pages → Build and deployment**, set
   **Source: Deploy from a branch**, **Branch: `main` / `root`**, then Save.
3. Your map goes live at `https://<you>.github.io/<repo>/`.

## Data source & refreshing

Coordinates and descriptions come from the Old-Growth Forest Network's public
Google My Maps layer (exported as KML and filtered to `State: Michigan`). To
refresh, re-export the network map and regenerate the `FORESTS` array in
`index.html`.
