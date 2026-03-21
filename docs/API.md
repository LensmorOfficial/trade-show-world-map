# Data Export & API Documentation

The trade show world map data is available in multiple formats for your own analysis, integrations, and applications.

## Data Formats

### JSON (Full Dataset)

```json
{
  "shows": [
    {
      "name": "MEDICA",
      "website": "https://www.medica.de",
      "city": "Düsseldorf",
      "country": "Germany",
      "venue": "Messe Düsseldorf",
      "start_date": "2026-11-16",
      "end_date": "2026-11-19",
      "frequency": "Annual",
      "industry": "Healthcare & Medical",
      "region": "Europe",
      "tier": 1,
      "lat": 51.2615,
      "lng": 6.7602
    }
  ]
}
```

**Download:** [data/shows.json](data/shows.json)

### CSV (Spreadsheet-friendly)

| Field | Description |
|-------|-------------|
| name | Official show name |
| website | Official website URL |
| city | Host city |
| country | Host country |
| venue | Exhibition venue |
| start_date | Start date (YYYY-MM-DD) |
| end_date | End date (YYYY-MM-DD) |
| frequency | Annual / Biennial / Triennial |
| industry | Industry category |
| region | Geographic region |
| tier | 1=Global flagship, 2=Regional leader, 3=Specialized |
| lat | Latitude |
| lng | Longitude |

**Download:** [data/shows.csv](data/shows.csv)

### Direct API Access

For programmatic access, the data is available at:

```
https://lensmorofficial.github.io/trade-show-world-map/data/shows.json
```

**Example: Fetch all Tier 1 healthcare shows**

```javascript
fetch('https://lensmorofficial.github.io/trade-show-world-map/data/shows.json')
  .then(r => r.json())
  .then(data => {
    const healthcareShows = data.shows.filter(s => 
      s.industry === 'Healthcare & Medical' && s.tier === 1
    );
    console.log(healthcareShows);
  });
```

**Example: Find shows in Q2 2026**

```javascript
fetch('https://lensmorofficial.github.io/trade-show-world-map/data/shows.json')
  .then(r => r.json())
  .then(data => {
    const q2Shows = data.shows.filter(s => {
      const date = new Date(s.start_date);
      return date >= new Date('2026-04-01') && date <= new Date('2026-06-30');
    });
    console.log(q2Shows);
  });
```

## Data License

The show data is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

You are free to:
- Use the data for any purpose, including commercial use
- Modify and build upon the data
- Distribute the data

Requirement:
- Attribution to Lensmor with a link to https://www.lensmor.com

Example attribution:
> Trade show data provided by [Lensmor](https://www.lensmor.com) under CC BY 4.0.

## Data Freshness

- **Update frequency:** Monthly
- **Last updated:** See commit history
- **Verification method:** Official show websites and verified industry sources

## Contributing Data

Found a show that's missing? See [CONTRIBUTING.md](../CONTRIBUTING.md) for how to add new shows or update existing entries.

## Use Cases

Common ways teams use this data:

- **Annual planning:** Import into spreadsheets for show selection scoring
- **CRM integration:** Enrich account records with upcoming relevant shows
- **Marketing automation:** Trigger campaigns based on show proximity
- **Sales intelligence:** Alert reps when target accounts are exhibiting
- **Competitive monitoring:** Track which shows competitors are attending

## Support

For data corrections, additions, or questions:
- Open an issue: https://github.com/LensmorOfficial/trade-show-world-map/issues
- Email: data@lensmor.com
