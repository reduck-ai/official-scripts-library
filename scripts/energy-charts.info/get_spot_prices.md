# Get Energy-Charts electricity spot prices

Automatically get Energy-Charts electricity spot prices on energy-charts.info. Read the Energy-Charts (Fraunhofer ISE) spot market chart of a European country for one week, month or year: the day-ahead auction price, and for Germany the intraday prices, gas price and fuel cost index, with the CO2 allowance price, the load, the production by group and the net cross-border trading over the same time steps. Use country "all" or "eu" to get the day-ahead price of every European bidding zone side by side (for example France next to Germany). Prices are in EUR/MWh and power in MW, each value at its UTC time. Time steps are 15 minutes where the market uses them (day-ahead since 1 October 2025) and hourly otherwise. The current week also holds the next day once its auction is published; later time steps are null. Data starts in 2015. A period with no published data fails with a message that says so.

- Site: energy-charts.info
- Address: `reduck/energy-charts.info/get_spot_prices`
- Updated: 2026-11-07 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/energy-charts.info/get_spot_prices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/energy-charts.info/get_spot_prices
```

## Input

- `year` (integer, required): Year of the period. For a week, the ISO week-numbering year.
- `country` (string, required): Country code in lowercase, as on Energy-Charts. "all" gives every European bidding zone's day-ahead price, "eu" those of the EU zones.
- `week` (integer, optional): ISO week number. Required when interval is week.
- `month` (integer, optional): Month number. Required when interval is month.
- `interval` (string, optional): The period the chart shows.
- `resolution` (string, optional): Germany (15min or 30min) and Switzerland (15min) only: a finer time step than the default hourly one. Other countries have one resolution, and this must be left out.

## Output

- `year` (integer, required)
- `times` (array, required): The UTC start of each time step (ISO 8601). values[i] of every series is at times[i].
- `series` (array, required)
- `country` (string, required)
- `interval` (string, required)
- `week` (integer | null, optional)
- `month` (integer | null, optional)
- `title` (string | null, optional): The chart title Energy-Charts shows.
- `source` (string | null, optional): The data source Energy-Charts names, e.g. ENTSO-E.
- `resolution` (string | null, optional)
- `updated_at` (string | null, optional): When Energy-Charts last updated the data (ISO 8601, UTC).

## FAQ

### What does "Get Energy-Charts electricity spot prices" do?

Read the Energy-Charts (Fraunhofer ISE) spot market chart of a European country for one week, month or year: the day-ahead auction price, and for Germany the intraday prices, gas price and fuel cost index, with the CO2 allowance price, the load, the production by group and the net cross-border trading over the same time steps. Use country "all" or "eu" to get the day-ahead price of every European bidding zone side by side (for example France next to Germany). Prices are in EUR/MWh and power in MW, each value at its UTC time. Time steps are 15 minutes where the market uses them (day-ahead since 1 October 2025) and hourly otherwise. The current week also holds the next day once its auction is published; later time steps are null. Data starts in 2015. A period with no published data fails with a message that says so.

### How do I automatically get Energy-Charts electricity spot prices on energy-charts.info?

Ask an AI agent connected to Reduck to run reduck/energy-charts.info/get_spot_prices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/energy-charts.info/get_spot_prices

### Is there a energy-charts.info API to get Energy-Charts electricity spot prices?

You do not need one. "Get Energy-Charts electricity spot prices" drives the real energy-charts.info pages in a browser, so it works whether or not energy-charts.info offers an API for this.

### What information do I need to provide?

Required: country, year. Optional: week, month, interval, resolution.

### What does it return?

It returns week, year, month, times, title, series, source, country, interval, resolution, updated_at.

### Do I need to be logged in to energy-charts.info?

No. It only uses pages of energy-charts.info that are reachable without signing in.

### Does it change anything on energy-charts.info, or only read data?

It only reads. It looks things up on energy-charts.info and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/energy-charts.info/get_spot_prices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/energy-charts.info/get_spot_prices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/energy-charts.info/get_spot_prices
