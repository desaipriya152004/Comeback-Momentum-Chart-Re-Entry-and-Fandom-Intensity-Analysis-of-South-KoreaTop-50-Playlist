# K-Pop Comeback Intelligence — Portfolio Web App

A deploy-ready portfolio web app built from the supplied South Korea Top 50 project artifacts.

## Included

- Responsive dark/neon portfolio UI
- Executive Overview
- Chart Re-entry Analysis
- Comeback Momentum
- Content Attribute Analysis
- Fandom Intensity
- Methodology & EDA
- Global artist, song, album-type and date filters
- Interactive Plotly charts
- Original Power BI screenshots
- Downloadable original project files:
  - `.pbix`
  - cleaned playlist CSV
  - re-entry event CSV
  - fandom leaderboard CSV
  - Python/Colab notebook
  - EDA report

## Analytical basis

The web app preserves the supplied project methodology:

1. Normalize song + artist IDs and validate 50 records per observed date.
2. Detect chart runs using consecutive observed dates.
3. Flag later runs as re-entry events.
4. Calculate re-entry gap, rank jump, popularity change, retention and days to best rank.
5. Calculate Momentum Spike Score using the supplied 40/20/20/20 weighting.
6. Calculate the Fandom Intensity Proxy from frequency, rank recovery, recovery speed and retention.

## Run locally

Because the dashboard loads JSON with `fetch()`, serve the folder with a local HTTP server.

### Python

```bash
cd kpop-analytics-portfolio
python -m http.server 8000
```

Open:

`http://localhost:8000`

## Deploy to GitHub Pages

1. Create a GitHub repository.
2. Upload the contents of this folder.
3. Go to **Settings → Pages**.
4. Select **Deploy from a branch**.
5. Select the `main` branch and `/root`.
6. Save and open the generated Pages URL.

## Deploy to Netlify

Drag the project folder into Netlify Drop, or connect the GitHub repository.

## Deploy to Vercel

Import the repository into Vercel. No build command is required; this is a static site.

## Portfolio positioning

Suggested project title:

**K-Pop Comeback Intelligence: Chart Re-entry, Momentum & Fandom Signals**

Suggested one-line description:

**An interactive analytics portfolio that turns 27,750 South Korea Top 50 playlist observations into measurable signals for chart re-entry, comeback intensity, content behavior and fandom reactivation.**

## Important interpretation note

The Fandom Intensity Proxy is a chart-behavior signal, not a direct measurement of fan count, sentiment or coordinated streaming. Momentum is a constructed index and can change under alternative weighting choices. The project supports descriptive/associational analysis rather than causal conclusions.
