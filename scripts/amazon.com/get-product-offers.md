# Get Amazon product offers from all sellers

Automatically get Amazon product offers from all sellers on amazon.com. See every seller offering an Amazon product, not just the one that won the buy box. Returns one page of Amazon's offer list (10 offers a page; page 1 also carries the buy-box offer), the total number of offers Amazon counts, and whether there is a next page. For each offer you get the price, item condition, seller name and id, seller rating and rating count, where the item ships from, and the delivery estimate. Prices, availability and delivery dates are pinned to a US ZIP code you choose. A seller can appear more than once when they list the same item under different conditions. A page past the last one returns no offers.

- Site: amazon.com
- Address: `reduck/amazon.com/get-product-offers`
- Updated: 2026-10-16 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product-offers
```

## Input

- `asin` (string, required): Amazon ASIN (or ISBN-10 for books), as it appears in /dp/<ASIN>.
- `page` (integer, optional): Page of the offer list, 10 offers each. Page 1 also carries the buy-box offer. has_next_page says when to stop.
- `zipCode` (string, optional): US ZIP used to pin the store location, which fixes prices, availability and delivery dates. Default 10001 (New York, NY).

## Output

- `url` (string, required)
- `asin` (string, required)
- `page` (integer, required)
- `offers` (array, required): This page's offers. On page 1 the buy-box offer comes first (position 0, is_buy_box true).
- `total_offers` (integer, required): Offers in Amazon's list for this product, all pages together, as Amazon counts them. The buy-box offer is shown apart from them.
- `has_next_page` (boolean, required)
- `zip` (string, optional)
- `title` (string | null, optional)

## FAQ

### What does "Get Amazon product offers from all sellers" do?

See every seller offering an Amazon product, not just the one that won the buy box. Returns one page of Amazon's offer list (10 offers a page; page 1 also carries the buy-box offer), the total number of offers Amazon counts, and whether there is a next page. For each offer you get the price, item condition, seller name and id, seller rating and rating count, where the item ships from, and the delivery estimate. Prices, availability and delivery dates are pinned to a US ZIP code you choose. A seller can appear more than once when they list the same item under different conditions. A page past the last one returns no offers.

### How do I automatically get Amazon product offers from all sellers on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product-offers

### Is there a amazon.com API to get Amazon product offers from all sellers?

You do not need one. "Get Amazon product offers from all sellers" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Required: asin. Optional: page, zipCode.

### What does it return?

It returns url, zip, asin, page, title, offers, total_offers, has_next_page.

### Do I need to be logged in to amazon.com?

No. It only uses pages of amazon.com that are reachable without signing in.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product-offers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/get-product-offers
