# Get Geizhals price history

Automatically get Geizhals price history on geizhals.de. Get the price history Geizhals.de shows for one product, by its Geizhals product id (from Search Geizhals products, or the number after -a in a product page link). Returns the product title, the lowest price on the page now and the number of offers, and for the period you choose (1 month, 3 months, 6 months, 1 year or the whole history) the lowest price of each day in euros from merchants in Germany, oldest first, counted back from the last day with a price. The statistics give the lowest and highest price of the whole history and its first and last dates. An unknown product id fails with a message that says so.

- Site: geizhals.de
- Address: `reduck/geizhals.de/get_price_history`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/geizhals.de/get_price_history`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/geizhals.de/get_price_history
```

## Input

- `product_id` (string, required): Geizhals product id, as Search Geizhals products returns it, or the number after -a in a product page link.
- `period` (string, optional): Period of the chart, as the site offers it: 1 month, 3 months, 6 months (the site's default), 1 year, or the whole history.

## Output

- `url` (string, required)
- `site` (string, required)
- `title` (string | null, required)
- `period` (string, required)
- `points` (array, required): The lowest price of each day, oldest first. Empty when Geizhals has no price history for the product.
- `product_id` (string, required)
- `statistics` (object | null, required): Lowest and highest price over the whole history the site holds, with its first and last dates.
- `currency` (string | null, optional)
- `offer_count` (integer | null, optional)
- `lowest_price_now` (number | null, optional): Lowest offer on the product page now.

## FAQ

### What does "Get Geizhals price history" do?

Get the price history Geizhals.de shows for one product, by its Geizhals product id (from Search Geizhals products, or the number after -a in a product page link). Returns the product title, the lowest price on the page now and the number of offers, and for the period you choose (1 month, 3 months, 6 months, 1 year or the whole history) the lowest price of each day in euros from merchants in Germany, oldest first, counted back from the last day with a price. The statistics give the lowest and highest price of the whole history and its first and last dates. An unknown product id fails with a message that says so.

### How do I automatically get Geizhals price history on geizhals.de?

Ask an AI agent connected to Reduck to run reduck/geizhals.de/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/geizhals.de/get_price_history

### Is there a geizhals.de API to get Geizhals price history?

You do not need one. "Get Geizhals price history" drives the real geizhals.de pages in a browser, so it works whether or not geizhals.de offers an API for this.

### What information do I need to provide?

Required: product_id. Optional: period.

### What does it return?

It returns url, site, title, period, points, currency, product_id, statistics, offer_count, lowest_price_now.

### Do I need to be logged in to geizhals.de?

No. It only uses pages of geizhals.de that are reachable without signing in.

### Does it change anything on geizhals.de, or only read data?

It only reads. It looks things up on geizhals.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/geizhals.de/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/geizhals.de/get_price_history

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/geizhals.de/get_price_history
