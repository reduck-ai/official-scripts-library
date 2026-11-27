# Get Amazon.in product offers from all sellers

Automatically get Amazon.in product offers from all sellers on amazon.in. See every seller offering an Amazon.in product, not just the one that won the buy box. Returns one page of Amazon's offer list (10 offers a page; page 1 also carries the buy-box offer), the total number of offers Amazon counts, and whether there is a next page. For each offer you get the price, item condition, seller name and id, seller rating and rating count, where the item ships from, and the delivery estimate. Prices, availability and delivery dates are pinned to an Indian postcode you choose. A seller can appear more than once when they list the same item under different conditions. A page past the last one returns no offers.

- Site: amazon.in
- Address: `reduck/amazon.in/get-product-offers`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.in/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.in/get-product-offers
```

## Input

- `asin` (string, required): Amazon ASIN (or ISBN-10 for books), as it appears in /dp/<ASIN>.
- `page` (integer, optional): Page of the offer list, 10 offers each. Page 1 also carries the buy-box offer.
- `zipCode` (string, optional): Indian postcode used to pin the store location. Default 110001 (New Delhi).

## Output

- `url` (string, required)
- `asin` (string, required)
- `page` (integer, required)
- `offers` (array, required)
- `total_offers` (integer, required)
- `has_next_page` (boolean, required)
- `zip` (string, optional)
- `title` (string | null, optional)

## FAQ

### What does "Get Amazon.in product offers from all sellers" do?

See every seller offering an Amazon.in product, not just the one that won the buy box. Returns one page of Amazon's offer list (10 offers a page; page 1 also carries the buy-box offer), the total number of offers Amazon counts, and whether there is a next page. For each offer you get the price, item condition, seller name and id, seller rating and rating count, where the item ships from, and the delivery estimate. Prices, availability and delivery dates are pinned to an Indian postcode you choose. A seller can appear more than once when they list the same item under different conditions. A page past the last one returns no offers.

### How do I automatically get Amazon.in product offers from all sellers on amazon.in?

Ask an AI agent connected to Reduck to run reduck/amazon.in/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.in/get-product-offers

### Is there a amazon.in API to get Amazon.in product offers from all sellers?

You do not need one. "Get Amazon.in product offers from all sellers" drives the real amazon.in pages in a browser, so it works whether or not amazon.in offers an API for this.

### What information do I need to provide?

Required: asin. Optional: page, zipCode.

### What does it return?

It returns url, zip, asin, page, title, offers, total_offers, has_next_page.

### Do I need to be logged in to amazon.in?

No. It only uses pages of amazon.in that are reachable without signing in.

### Does it change anything on amazon.in, or only read data?

It only reads. It looks things up on amazon.in and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.in/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.in/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.in/get-product-offers
