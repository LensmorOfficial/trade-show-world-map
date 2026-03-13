# 🌍 Global B2B Trade Show Map

[![Shows](https://img.shields.io/badge/Shows-200-6b75ff?style=flat-square)](https://lensmorofficial.github.io/trade-show-world-map/)
[![GitHub Stars](https://img.shields.io/github/stars/LensmorOfficial/trade-show-world-map?style=flat-square)](https://github.com/LensmorOfficial/trade-show-world-map/stargazers)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey?style=flat-square)](https://creativecommons.org/licenses/by/4.0/)

**[View Interactive Map →](https://lensmorofficial.github.io/trade-show-world-map/)**

An interactive world map of **200 major global B2B trade shows** across 60+ countries. Filter by industry, region, tier, and month to find the right events for your business.

![Map Preview](https://lensmorofficial.github.io/trade-show-world-map/preview.png)

## Features

- **Interactive world map** powered by Leaflet.js with dark CartoDB tiles
- **200 verified B2B trade shows** with venues, dates, and official websites
- **Filter by** region, industry, tier, month, and keyword search
- **3-tier system** — Tier 1 (top global), Tier 2 (regional leaders), Tier 3 (specialized)
- **Marker clustering** for clean visualization at any zoom level
- Works entirely in-browser — no backend required

## Data Schema

Each show entry includes:

| Field | Description |
|-------|-------------|
| `name` | Official show name |
| `website` | Official website URL |
| `city` / `country` | Location |
| `venue` | Exhibition hall / convention center |
| `start_date` / `end_date` | Event dates (ISO 8601) |
| `frequency` | Annual / Biennial / Triennial |
| `industry` | Industry category |
| `region` | North America / Europe / Asia / Middle East & Africa / Latin America |
| `tier` | 1 = Top Global, 2 = Regional Leader, 3 = Specialized |
| `lat` / `lng` | Coordinates for map plotting |

## Industries Covered

Technology & Electronics · Healthcare & Medical · Manufacturing & Industrial · Food & Beverage · Automotive · Energy & Environment · Logistics & Supply Chain · Finance & Fintech · Retail · Construction & Building Materials · Packaging · Pharmaceutical · Aerospace & Defense · Beauty & Personal Care · Fashion & Textiles · Real Estate · Agriculture · Travel & Tourism · Marketing & Advertising · Cybersecurity · Defense · Education

## Geographic Coverage

| Region | Shows |
|--------|-------|
| Europe | ~72 |
| North America | ~53 |
| Asia | ~38 |
| Middle East & Africa | ~22 |
| Latin America | ~15 |

## Local Development

```bash
# Clone the repo
git clone https://github.com/LensmorOfficial/trade-show-world-map.git
cd trade-show-world-map

# Serve locally (required for fetch() to work)
python3 -m http.server 8000
# then open http://localhost:8000
```

## Contributing

Found a missing show or incorrect data? PRs welcome!

1. Edit `data/b2b_shows.json`
2. Follow the existing schema
3. Submit a pull request

## License

Data is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code is MIT.

---

## About

Built and maintained by [Lensmor](https://www.lensmor.com/?utm_source=github&utm_medium=readme&utm_campaign=trade-show-world-map) — the trade show intelligence platform for exhibitors and event marketers.

**[Try Lensmor Free →](https://www.lensmor.com/?utm_source=github&utm_medium=readme&utm_campaign=trade-show-world-map)**
