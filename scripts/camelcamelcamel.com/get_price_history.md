# Get CamelCamelCamel Amazon price history

Automatically get CamelCamelCamel Amazon price history on camelcamelcamel.com. Get the Amazon price history CamelCamelCamel holds for one product, by ASIN or Amazon link, on the Amazon country you choose (US, UK, Germany, France, Italy, Spain, Canada, Australia). For each price type it tracks (sold by Amazon, third-party new, third-party used) you get the lowest and highest price ever with their dates, the current price with the date it was seen, and the average, in the country's currency. Also returns the product title, image, the product details CamelCamelCamel lists, and the link to its price chart image for the period you choose. A product CamelCamelCamel has no history for returns an empty list of price types; a current price of null means that offer is not available now.

- Site: camelcamelcamel.com
- Address: `reduck/camelcamelcamel.com/get_price_history`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/camelcamelcamel.com/get_price_history`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/camelcamelcamel.com/get_price_history
```

## Input

- `product` (string, required): The product's ASIN (for example B0BDHWDR12), an Amazon product link, or a CamelCamelCamel product link.
- `country` (string, optional): The Amazon country whose prices to read.
- `chart_period` (string, optional): Period the returned chart image covers. The price table always covers the whole history.

## Output

- `url` (string, required)
- `asin` (string, required)
- `prices` (array, required)
- `country` (string, required)
- `title` (string | null, optional)
- `details` (object, optional): The product details CamelCamelCamel lists (manufacturer, model, EAN, list price, last update...), keyed by their label as the site writes it.
- `chart_url` (string | null, optional): PNG chart of the price history for chart_period, as CamelCamelCamel draws it.
- `image_url` (string | null, optional)

## FAQ

### What does "Get CamelCamelCamel Amazon price history" do?

Get the Amazon price history CamelCamelCamel holds for one product, by ASIN or Amazon link, on the Amazon country you choose (US, UK, Germany, France, Italy, Spain, Canada, Australia). For each price type it tracks (sold by Amazon, third-party new, third-party used) you get the lowest and highest price ever with their dates, the current price with the date it was seen, and the average, in the country's currency. Also returns the product title, image, the product details CamelCamelCamel lists, and the link to its price chart image for the period you choose. A product CamelCamelCamel has no history for returns an empty list of price types; a current price of null means that offer is not available now.

### How do I automatically get CamelCamelCamel Amazon price history on camelcamelcamel.com?

Ask an AI agent connected to Reduck to run reduck/camelcamelcamel.com/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/camelcamelcamel.com/get_price_history

### Is there a camelcamelcamel.com API to get CamelCamelCamel Amazon price history?

You do not need one. "Get CamelCamelCamel Amazon price history" drives the real camelcamelcamel.com pages in a browser, so it works whether or not camelcamelcamel.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: country, chart_period.

### What does it return?

It returns url, asin, title, prices, country, details, chart_url, image_url.

### Do I need to be logged in to camelcamelcamel.com?

No. It only uses pages of camelcamelcamel.com that are reachable without signing in.

### Does it change anything on camelcamelcamel.com, or only read data?

It only reads. It looks things up on camelcamelcamel.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/camelcamelcamel.com/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/camelcamelcamel.com/get_price_history

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/camelcamelcamel.com/get_price_history
