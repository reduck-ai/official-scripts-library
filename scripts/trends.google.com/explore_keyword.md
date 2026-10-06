# Google Trends API: compare keywords and get related queries

Automatically compare keywords and get related queries on trends.google.com. See which of up to five terms gets more search interest, over time and by region.

- Site: trends.google.com
- Address: `reduck/trends.google.com/explore_keyword`
- Updated: 2026-10-05 (v3)
- Author: Reduck AI (reduck)

## About

Google Trends scales each result to the peak of that one request, so terms only compare fairly when fetched together. A US camping gear shop planning spring ads could send ["tent", "hammock", "sleeping bag"] with geo "US" and date "today 5-y", then read interestOverTime to see when each tops out, year after year. With two or more terms, regionShare splits interest by state, showing where hammocks beat tents. Related topics need a single term, so a second call with "hammock" alone adds them, and a rising query marked Breakout (over 5000% growth) can earn its own ad group. These are indexes, not search counts: a low-volume term reads 0 beside bigger ones, and if every term is that small the timeline comes back empty. Labels and region names come back in English whatever geo you pick. As of early October 2026, every run on Reduck's hosted browsers had failed, so use the Reduck extension in your own Chrome.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trends.google.com/explore_keyword`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trends.google.com/explore_keyword
```

## Input

- `keywords` (array, required): 1-5 search terms and/or Trends topic mids (e.g. "/g/11khcfz0y2") compared in a single query — values are relative to the shared peak, so this is the only way to compare terms. Terms must not contain commas (the site's own separator).
- `geo` (string, optional): ISO region code: "US", "FR", "US-CA"… Empty string = worldwide.
- `date` (string, optional): Trends range: "now 1-H", "now 4-H", "now 1-d", "now 7-d", "today 1-m", "today 3-m", "today 12-m", "today 5-y", "all", or explicit "YYYY-MM-DD YYYY-MM-DD".
- `category` (integer, optional): Trends category id (0 = all categories). Same ids as the site's category picker.
- `property` (string, optional): Search property: "" = web search, images, news, froogle (shopping), youtube.

## Output

- `geo` (string, required)
- `date` (string, required)
- `keywords` (array, required)
- `byKeyword` (array, required): Per-keyword panels, aligned with keywords. relatedTopics is null in compare mode — the site drops that panel when comparing.
- `regionShare` (array, required): Compare mode only (2+ keywords), else []: each keyword's share (%) of combined interest per region, shares[i] aligns with keywords[i].
- `interestOverTime` (array, required): Relative interest 0-100, shared scale across all keywords (100 = the overall peak). values[i] aligns with keywords[i]. Empty for insufficient volume.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "geo": "…",
  "date": "2026-01-15T09:30:00Z",
  "keywords": [
    "…"
  ],
  "byKeyword": [
    {
      "keyword": "…",
      "relatedTopics": {
        "top": [
          {}
        ],
        "rising": [
          {}
        ]
      },
      "relatedQueries": {
        "top": [
          {}
        ],
        "rising": [
          {}
        ]
      },
      "interestByRegion": [
        {
          "value": 3,
          "geoCode": "…",
          "geoName": "…"
        }
      ]
    }
  ],
  "regionShare": [
    {
      "shares": [
        3
      ],
      "geoCode": "…",
      "geoName": "…"
    }
  ],
  "interestOverTime": [
    {
      "date": "2026-01-15T09:30:00Z",
      "time": 3,
      "values": [
        3
      ]
    }
  ]
}
```

## FAQ

### What does "Google Trends API: compare keywords and get related queries" do?

An unofficial Google Trends API: compare up to 5 keywords' search interest over time and by region, and get their top and rising related queries, as data in one call. Google Trends explore for 1-5 keywords in one compare query: interest over time (shared scale), interest by region, per-region share %, related topics and queries (top + rising), for a given geo/date range/category/property.

### How do I automatically compare keywords and get related queries on trends.google.com?

Ask an AI agent connected to Reduck to run reduck/trends.google.com/explore_keyword, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trends.google.com/explore_keyword

### Is there a trends.google.com API to compare keywords and get related queries?

You do not need one. "Google Trends API: compare keywords and get related queries" drives the real trends.google.com pages in a browser, so it works whether or not trends.google.com offers an API for this.

### What information do I need to provide?

Required: keywords. Optional: geo, date, category, property.

### What does it return?

It returns geo, date, keywords, byKeyword, regionShare, interestOverTime.

### Do I need to be logged in to trends.google.com?

No. It only uses pages of trends.google.com that are reachable without signing in.

### Does it change anything on trends.google.com, or only read data?

It only reads. It looks things up on trends.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trends.google.com/explore_keyword, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trends.google.com/explore_keyword

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I compare more than five keywords in Google Trends at once?

The keywords field takes at most five terms, the same limit as Google's classic Explore page, which explore_keyword opens. The redesigned Explore page in the browser goes up to 8 groups of terms. For a longer list, keep one anchor term in every batch of five and rescale the others against it, since each call sets its own 100.

### What happens if Google Trends returns 429 Too Many Requests?

When Google answers the explore request with an error such as HTTP 429, the run stops with an error that says so instead of returning partial data, so wait a while and retry. The run also fails if the charts have not all loaded within 20 seconds.

### How is this different from Google's official Trends API alpha?

Google's Trends API, announced in July 2025, is still an alpha in October 2026: access goes through an application form for testers, and its page lists no price. That API serves a rolling five years at daily or coarser intervals and lets you merge requests to compare dozens of terms. explore_keyword reads the public explore page instead, so it needs no application and also takes date "all" or hour ranges such as "now 4-H".

### How can I tell whether a trending Google search is seasonal?

Take a term from trending_now, which lists what is spiking in one country over the last 4 hours to 7 days, and run explore_keyword on it with date "today 5-y", because the default 12-month window cannot show a peak that returns each year. A one-off spike shows a single peak, while a seasonal term rises around the same weeks every year. The breakdown terms trending_now returns for each trend can go straight into keywords, up to five per call.

Source: https://reduck.ai/explore/scripts/reduck/trends.google.com/explore_keyword
