# Get Amazon.es product offers from all sellers

Automatically get Amazon.es product offers from all sellers on amazon.es. List every seller offering an Amazon.es product, one page of 10 offers at a time: price in euros, condition, seller name and id, seller rating, ships-from and delivery estimate. Page 1 also carries the buy-box offer. Prices are pinned to a Spanish postcode.

- Site: amazon.es
- Address: `reduck/amazon.es/get-product-offers`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/get-product-offers
```

## Input

- `asin` (string, required): Amazon ASIN, as in /dp/<ASIN>.
- `page` (integer, optional): Page of the offer list, 10 offers each.
- `zipCode` (string, optional): Spanish postcode used to pin the store location.

## Output

- `url` (string, required)
- `asin` (string, required)
- `page` (integer, required)
- `offers` (array, required)
- `total_offers` (integer | null, required): Offers Amazon counts for the product; null when the page does not show the count.
- `has_next_page` (boolean, required)
- `zip` (string, optional)
- `title` (string | null, optional)

## FAQ

### What does "Get Amazon.es product offers from all sellers" do?

List every seller offering an Amazon.es product, one page of 10 offers at a time: price in euros, condition, seller name and id, seller rating, ships-from and delivery estimate. Page 1 also carries the buy-box offer. Prices are pinned to a Spanish postcode.

### How do I automatically get Amazon.es product offers from all sellers on amazon.es?

Ask an AI agent connected to Reduck to run reduck/amazon.es/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/get-product-offers

### Is there a amazon.es API to get Amazon.es product offers from all sellers?

You do not need one. "Get Amazon.es product offers from all sellers" drives the real amazon.es pages in a browser, so it works whether or not amazon.es offers an API for this.

### What information do I need to provide?

Required: asin. Optional: page, zipCode.

### What does it return?

It returns url, zip, asin, page, title, offers, total_offers, has_next_page.

### Do I need to be logged in to amazon.es?

No. It only uses pages of amazon.es that are reachable without signing in.

### Does it change anything on amazon.es, or only read data?

It only reads. It looks things up on amazon.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/get-product-offers
