# StormSight — AI-Powered Cyclone Intelligence Dashboard

StormShield is a frontend prototype built for Smart India Hackathon 2026: an AI/ML decision-support dashboard for detecting, classifying, and forecasting tropical cyclones in the North Indian Ocean basin.

This repo is a **single self-contained static page** (`index.html`) — no build step, no dependencies to install. It runs entirely on synthetic demo data and is structured so a real backend (REST API / FastAPI / Node.js) can be plugged in later through the `api` layer inside `index.html`.

## Run locally

Just open `index.html` in a browser, or serve it with any static file server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy on Render (Static Site)

1. Push this repo to GitHub (see below).
2. On [render.com](https://render.com), click **New +** → **Static Site**.
3. Connect this GitHub repo.
4. Settings:
   - **Build Command:** (leave empty)
   - **Publish Directory:** `.`
5. Click **Create Static Site**. Render will give you a live URL in a minute or two.

## Notes

- All data shown (storms, alerts, satellite imagery, historical tracks, system status) is **clearly labeled demo/mock data**.
- The mock API functions (`getActiveStorms`, `getStormDetails`, `getForecast`, `getSatelliteData`, `getAlerts`, `getHistoricalStorms`, `getModelStatus`) live near the top of the `<script type="text/babel">` block in `index.html` — replace their internals with real `fetch()` calls once a backend is available.
- This is a decision-support prototype, not a replacement for official IMD forecasts or warnings.
