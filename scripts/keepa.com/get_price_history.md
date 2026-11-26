# Get Keepa Amazon price history

Automatically get Keepa Amazon price history on keepa.com. Get the Amazon price history Keepa shows for one product, by ASIN or Amazon link, on one of 11 Amazon countries (US, UK, Germany, France, Japan, Canada, Italy, Spain, India, Mexico, Brazil). Returns the product title, images, when Keepa started tracking it and last updated it, and the price series a visitor sees on Keepa's chart for the period you choose: Buy Box, Amazon, new, used, list price, Lightning Deals, Amazon Warehouse, new sold by Amazon (FBA), new shipped by the seller (FBM), refurbished, collectible, and each used condition. Each series is a list of points (time, price in the country's currency, shipping when Keepa records it); a null price means no offer at that time. Series with no point in the period are left out. Sales rank is not included, as Keepa shows it only to subscribers.

- Site: keepa.com
- Address: `reduck/keepa.com/get_price_history`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/keepa.com/get_price_history`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/keepa.com/get_price_history
```

## Input

- `product` (string, required): The product's ASIN (for example B0BDHWDR12) or an Amazon product link.
- `range` (string, optional): Period of the series, as the chart's range buttons offer it. Keepa's chart opens on 3 months.
- `country` (string, optional): The Amazon country whose prices to read.

## Output

- `url` (string, required)
- `asin` (string, required)
- `series` (object, required): Price series by name: buy_box, amazon, new, used, list_price, lightning_deal, warehouse, new_fba, new_fbm, refurbished, collectible, used_like_new, used_very_good, used_good, used_acceptable, buy_box_used.
- `country` (string, required)
- `title` (string | null, optional)
- `images` (array, optional)
- `last_update` (string | null, optional)
- `manufacturer` (string | null, optional)
- `tracking_since` (string | null, optional)
- `last_price_change` (string | null, optional)

## FAQ

### What does "Get Keepa Amazon price history" do?

Get the Amazon price history Keepa shows for one product, by ASIN or Amazon link, on one of 11 Amazon countries (US, UK, Germany, France, Japan, Canada, Italy, Spain, India, Mexico, Brazil). Returns the product title, images, when Keepa started tracking it and last updated it, and the price series a visitor sees on Keepa's chart for the period you choose: Buy Box, Amazon, new, used, list price, Lightning Deals, Amazon Warehouse, new sold by Amazon (FBA), new shipped by the seller (FBM), refurbished, collectible, and each used condition. Each series is a list of points (time, price in the country's currency, shipping when Keepa records it); a null price means no offer at that time. Series with no point in the period are left out. Sales rank is not included, as Keepa shows it only to subscribers.

### How do I automatically get Keepa Amazon price history on keepa.com?

Ask an AI agent connected to Reduck to run reduck/keepa.com/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/keepa.com/get_price_history

### Is there a keepa.com API to get Keepa Amazon price history?

You do not need one. "Get Keepa Amazon price history" drives the real keepa.com pages in a browser, so it works whether or not keepa.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: range, country.

### What does it return?

It returns url, asin, title, images, series, country, last_update, manufacturer, tracking_since, last_price_change.

### Do I need to be logged in to keepa.com?

No. It only uses pages of keepa.com that are reachable without signing in.

### Does it change anything on keepa.com, or only read data?

It only reads. It looks things up on keepa.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/keepa.com/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/keepa.com/get_price_history

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/keepa.com/get_price_history
