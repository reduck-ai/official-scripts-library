# Get Energy-Charts cross-border electricity exchanges

Automatically get Energy-Charts cross-border electricity exchanges on energy-charts.info. Read the Energy-Charts (Fraunhofer ISE) import and export chart of a European country for a year, half-year, quarter, meteorological season or month: the electricity, in GWh, that each country of the chart exported to each other one, for the country and its neighbours. Choose the scheduled commercial exchanges (cross-border trading, the default) or the measured physical flows. Use country "all" or "eu" for every European country or the EU. Each exchange is one direction (from, to), so a border has up to two; pairs with no exchange are left out, so a future period gives an empty list. Data starts in 2015.

- Site: energy-charts.info
- Address: `reduck/energy-charts.info/get_cross_border_exchanges`
- Updated: 2026-11-07 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/energy-charts.info/get_cross_border_exchanges`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/energy-charts.info/get_cross_border_exchanges
```

## Input

- `year` (integer, required): Year of the period. A winter season starts in December of this year.
- `country` (string, required): Country code in lowercase, as on Energy-Charts. "all" gives every European country, "eu" the European Union with its neighbours.
- `flow` (string, optional): commercial: the scheduled commercial exchanges (cross-border trading). physical: the measured physical flows.
- `period` (integer, optional): Which part of the year, required unless interval is year: half-year 1 or 2, quarter 1 to 4, season 1 (spring), 2 (summer), 3 (autumn) or 4 (winter), month 1 to 12.
- `interval` (string, optional): The period the chart covers.

## Output

- `flow` (string, required)
- `unit` (string, required): GWh.
- `year` (integer, required)
- `country` (string, required)
- `interval` (string, required)
- `countries` (array, required): Every country of the chart.
- `exchanges` (array, required)
- `title` (string | null, optional): The chart title Energy-Charts shows.
- `period` (integer | null, optional)
- `source` (string | null, optional): The data source Energy-Charts names.
- `updated_at` (string | null, optional): When Energy-Charts last updated the data (ISO 8601, UTC).

## FAQ

### What does "Get Energy-Charts cross-border electricity exchanges" do?

Read the Energy-Charts (Fraunhofer ISE) import and export chart of a European country for a year, half-year, quarter, meteorological season or month: the electricity, in GWh, that each country of the chart exported to each other one, for the country and its neighbours. Choose the scheduled commercial exchanges (cross-border trading, the default) or the measured physical flows. Use country "all" or "eu" for every European country or the EU. Each exchange is one direction (from, to), so a border has up to two; pairs with no exchange are left out, so a future period gives an empty list. Data starts in 2015.

### How do I automatically get Energy-Charts cross-border electricity exchanges on energy-charts.info?

Ask an AI agent connected to Reduck to run reduck/energy-charts.info/get_cross_border_exchanges, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/energy-charts.info/get_cross_border_exchanges

### Is there a energy-charts.info API to get Energy-Charts cross-border electricity exchanges?

You do not need one. "Get Energy-Charts cross-border electricity exchanges" drives the real energy-charts.info pages in a browser, so it works whether or not energy-charts.info offers an API for this.

### What information do I need to provide?

Required: country, year. Optional: flow, period, interval.

### What does it return?

It returns flow, unit, year, title, period, source, country, interval, countries, exchanges, updated_at.

### Do I need to be logged in to energy-charts.info?

No. It only uses pages of energy-charts.info that are reachable without signing in.

### Does it change anything on energy-charts.info, or only read data?

It only reads. It looks things up on energy-charts.info and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/energy-charts.info/get_cross_border_exchanges, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/energy-charts.info/get_cross_border_exchanges

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/energy-charts.info/get_cross_border_exchanges
