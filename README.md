# nook-tv

Standalone kiosk display for **HyperBase Intel** — a 1080×1920 portrait TV loop that cycles fresh AI-curated news across hyperscalers, agentic AI, and quantum computing.

Extracted from the `Hyperbase-Lobby` `/the-nook` route so it can run on its own display without the front-door lobby loop.

## Run

```bash
cp .env.example .env.local   # add PERPLEXITY_API_KEY
npm install
npm run dev
```

Then open `http://localhost:3000`.

## Data

`/api/news` fans out to Perplexity `sonar-pro` across three topics, caches the last-good payload to disk, and refreshes daily at 09:00 CT. Force a refetch with `?refresh=1`.
