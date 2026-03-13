# Contributing to Global B2B Trade Show Map

Thank you for helping keep this dataset accurate and comprehensive.

## How to contribute

- **Add a missing show** — open an issue using the "Add Trade Show" template or submit a PR
- **Fix incorrect data** — open an issue using the "Data Error" template or submit a PR directly
- **Improve the map UI** — open a PR with your changes to `index.html`

## Data format

All entries live in `data/b2b_shows.json`. Each entry must include:

| Field | Type | Example |
|-------|------|---------|
| `name` | string | `"CES"` |
| `website` | string | `"https://www.ces.tech"` |
| `city` | string | `"Las Vegas"` |
| `country` | string | `"USA"` |
| `venue` | string | `"Las Vegas Convention Center"` |
| `start_date` | string (YYYY-MM-DD) | `"2026-01-06"` |
| `end_date` | string (YYYY-MM-DD) | `"2026-01-09"` |
| `frequency` | string | `"Annual"` |
| `industry` | string | `"Technology & Electronics"` |
| `region` | string | `"North America"` |
| `tier` | number (1-3) | `1` |
| `lat` | number | `36.1215` |
| `lng` | number | `-115.1739` |

### Region values

`North America` / `Europe` / `Asia` / `Middle East & Africa` / `Latin America`

### Tier definitions

- **Tier 1** — Top global shows (major international attendance, 10,000+ exhibitors or equivalent)
- **Tier 2** — Regional leaders (strong industry presence, established history)
- **Tier 3** — Specialized or emerging shows

## Pull request checklist

- [ ] Entry is in alphabetical order within its region (not required, but preferred)
- [ ] All required fields are populated
- [ ] `website` is the official show website (not a ticketing or travel site)
- [ ] `lat` / `lng` are accurate (can use Google Maps to verify)
- [ ] JSON is valid (run `python3 -m json.tool data/b2b_shows.json` to verify)

## Code of conduct

Be respectful. Focus on factual accuracy. No promotional content in data fields.

---

Maintained by [Lensmor](https://www.lensmor.com/?utm_source=github&utm_medium=contributing&utm_campaign=trade-show-world-map) — trade show intelligence for B2B teams.
