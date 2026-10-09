# tardis-data

Created at 2026-10-08

Daily snapshot of the [Tardis](https://tardis.hi-curio.com) history timeline

- `timeline.json`: `{ groups, items }`. Years are astronomical (1 BCE = 0). Labels and notes are
  keyed by language name (`english`, `chinese`, `spanish`, …).
- `.github/workflows/refresh.yml`: fetches daily at 03:17 UTC (or run it by hand). It commits and rebuilds tardis 
  only when the data changed.

Tardis builds its region pages (`/history/…`) from this file via `TIMELINE_URL`:
https://raw.githubusercontent.com/Eyasics/tardis-data/main/timeline.json
