# Get idealo.it price history

Automatically get idealo.it price history on idealo.it. Get the price history idealo.it shows for one product, by its idealo product id (from search_products, or the number in a product page link). Returns the product title, the lowest price on the page now and the number of offers, and for the period you choose (1 month, 3 months, 6 months or 1 year) the lowest price of each day in euros, oldest first, with the figures the chart shows: average, lowest and highest price, and how many days ago the lowest and highest were. When the site marks the product as a bargain, the answer also gives the price it compares with and the saving. A product with no recorded price returns an empty list. An unknown product id fails with a message that says so.

- Site: idealo.it
- Address: `reduck/idealo.it/get_price_history`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/idealo.it/get_price_history`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/idealo.it/get_price_history
```

## Input

- `product_id` (string, required): idealo product id, as search_products returns it, or the number in a product page link.
- `period` (string, optional): Period of the chart, as the site offers it: 1 month, 3 months (the default), 6 months or 1 year.

## Output

- `url` (string, required)
- `site` (string, required)
- `title` (string | null, required)
- `period` (string, required)
- `points` (array, required): The lowest price of each day, oldest first. Days with no offer are left out. Empty when idealo has no price history for the product.
- `bargain` (object | null, required): When the site marks the product as a bargain: the price now, the lowest average price of the last 90 days it compares with, and the saving. Null otherwise.
- `product_id` (string, required)
- `statistics` (object | null, required): The figures the chart shows for the period. Null with no history.
- `currency` (string | null, optional)
- `offer_count` (integer | null, optional)
- `lowest_price_now` (number | null, optional): Lowest offer on the product page now.

## FAQ

### What does "Get idealo.it price history" do?

Get the price history idealo.it shows for one product, by its idealo product id (from search_products, or the number in a product page link). Returns the product title, the lowest price on the page now and the number of offers, and for the period you choose (1 month, 3 months, 6 months or 1 year) the lowest price of each day in euros, oldest first, with the figures the chart shows: average, lowest and highest price, and how many days ago the lowest and highest were. When the site marks the product as a bargain, the answer also gives the price it compares with and the saving. A product with no recorded price returns an empty list. An unknown product id fails with a message that says so.

### How do I automatically get idealo.it price history on idealo.it?

Ask an AI agent connected to Reduck to run reduck/idealo.it/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/idealo.it/get_price_history

### Is there a idealo.it API to get idealo.it price history?

You do not need one. "Get idealo.it price history" drives the real idealo.it pages in a browser, so it works whether or not idealo.it offers an API for this.

### What information do I need to provide?

Required: product_id. Optional: period.

### What does it return?

It returns url, site, title, period, points, bargain, currency, product_id, statistics, offer_count, lowest_price_now.

### Do I need to be logged in to idealo.it?

No. It only uses pages of idealo.it that are reachable without signing in.

### Does it change anything on idealo.it, or only read data?

It only reads. It looks things up on idealo.it and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/idealo.it/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/idealo.it/get_price_history

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/idealo.it/get_price_history
