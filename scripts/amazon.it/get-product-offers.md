# Get Amazon.it product offers from all sellers

Automatically get Amazon.it product offers from all sellers on amazon.it. List every seller offering an Amazon.it product, one page of 10 offers at a time: price as the page shows it, condition, seller name and id, seller rating, ships-from and delivery estimate. Page 1 also carries the buy-box offer. Prices are pinned to an Italian postcode.

- Site: amazon.it
- Address: `reduck/amazon.it/get-product-offers`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.it/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.it/get-product-offers
```

## Input

- `asin` (string, required): Amazon ASIN, as in /dp/<ASIN>.
- `page` (integer, optional): Page of the offer list, 10 offers each.
- `zipCode` (string, optional): Italian postcode used to pin the store location.

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

### What does "Get Amazon.it product offers from all sellers" do?

List every seller offering an Amazon.it product, one page of 10 offers at a time: price as the page shows it, condition, seller name and id, seller rating, ships-from and delivery estimate. Page 1 also carries the buy-box offer. Prices are pinned to an Italian postcode.

### How do I automatically get Amazon.it product offers from all sellers on amazon.it?

Ask an AI agent connected to Reduck to run reduck/amazon.it/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.it/get-product-offers

### Is there a amazon.it API to get Amazon.it product offers from all sellers?

You do not need one. "Get Amazon.it product offers from all sellers" drives the real amazon.it pages in a browser, so it works whether or not amazon.it offers an API for this.

### What information do I need to provide?

Required: asin. Optional: page, zipCode.

### What does it return?

It returns url, zip, asin, page, title, offers, total_offers, has_next_page.

### Do I need to be logged in to amazon.it?

No. It only uses pages of amazon.it that are reachable without signing in.

### Does it change anything on amazon.it, or only read data?

It only reads. It looks things up on amazon.it and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.it/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.it/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.it/get-product-offers
