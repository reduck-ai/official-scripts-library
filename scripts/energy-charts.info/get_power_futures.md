# Get Energy-Charts electricity futures prices

Automatically get Energy-Charts electricity futures prices on energy-charts.info. Read the Energy-Charts (Fraunhofer ISE) electricity futures chart for Germany, France, Austria or Switzerland: the daily settlement price, in EUR/MWh, of each base-load contract for a delivery year, quarter, month or week (for example "2027", "Q1 2027", "01.2027"), on each trading day. This is what the market pays today for power delivered later, so it shows the expected cost ahead. A contract has a null price on the days it was not traded, before it opened or after its delivery started. Pass from and to (trading dates) to get only a range of trading days, as the chart's date range selector does. Without them, every trading day since 2021 is returned, which is a large answer. A range where the site has no trading days gives empty lists.

- Site: energy-charts.info
- Address: `reduck/energy-charts.info/get_power_futures`
- Updated: 2026-11-07 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/energy-charts.info/get_power_futures`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/energy-charts.info/get_power_futures
```

## Input

- `country` (string, required): Country code in lowercase.
- `to` (string, optional): Last trading day to return (YYYY-MM-DD), as the chart's date range selector.
- `from` (string, optional): First trading day to return (YYYY-MM-DD), as the chart's date range selector.
- `product` (string, optional): The delivery period of the contracts.

## Output

- `country` (string, required)
- `product` (string, required)
- `contracts` (array, required)
- `trading_days` (array, required): Trading days (YYYY-MM-DD), oldest first. prices[i] of every contract is on trading_days[i].
- `unit` (string | null, optional): Unit of the prices, EUR/MWh.
- `title` (string | null, optional): The chart title Energy-Charts shows.
- `source` (string | null, optional): The data source Energy-Charts names.
- `updated_at` (string | null, optional): When Energy-Charts last updated the data (ISO 8601, UTC).

## FAQ

### What does "Get Energy-Charts electricity futures prices" do?

Read the Energy-Charts (Fraunhofer ISE) electricity futures chart for Germany, France, Austria or Switzerland: the daily settlement price, in EUR/MWh, of each base-load contract for a delivery year, quarter, month or week (for example "2027", "Q1 2027", "01.2027"), on each trading day. This is what the market pays today for power delivered later, so it shows the expected cost ahead. A contract has a null price on the days it was not traded, before it opened or after its delivery started. Pass from and to (trading dates) to get only a range of trading days, as the chart's date range selector does. Without them, every trading day since 2021 is returned, which is a large answer. A range where the site has no trading days gives empty lists.

### How do I automatically get Energy-Charts electricity futures prices on energy-charts.info?

Ask an AI agent connected to Reduck to run reduck/energy-charts.info/get_power_futures, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/energy-charts.info/get_power_futures

### Is there a energy-charts.info API to get Energy-Charts electricity futures prices?

You do not need one. "Get Energy-Charts electricity futures prices" drives the real energy-charts.info pages in a browser, so it works whether or not energy-charts.info offers an API for this.

### What information do I need to provide?

Required: country. Optional: to, from, product.

### What does it return?

It returns unit, title, source, country, product, contracts, updated_at, trading_days.

### Do I need to be logged in to energy-charts.info?

No. It only uses pages of energy-charts.info that are reachable without signing in.

### Does it change anything on energy-charts.info, or only read data?

It only reads. It looks things up on energy-charts.info and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/energy-charts.info/get_power_futures, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/energy-charts.info/get_power_futures

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/energy-charts.info/get_power_futures
