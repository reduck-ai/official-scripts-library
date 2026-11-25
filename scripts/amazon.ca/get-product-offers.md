# Get Amazon.ca product offers from all sellers

Automatically get Amazon.ca product offers from all sellers on amazon.ca. List every seller offering an Amazon.ca product, one page of 10 offers at a time: price as the page shows it, condition, seller name and id, seller rating, ships-from and delivery estimate. Page 1 also carries the buy-box offer. Prices are pinned to a Canadian postal code.

- Site: amazon.ca
- Address: `reduck/amazon.ca/get-product-offers`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.ca/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.ca/get-product-offers
```

## Input

- `asin` (string, required): Amazon ASIN, as in /dp/<ASIN>.
- `page` (integer, optional): Page of the offer list, 10 offers each.
- `zipCode` (string, optional): Canadian postal code used to pin the store location.

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

### What does "Get Amazon.ca product offers from all sellers" do?

List every seller offering an Amazon.ca product, one page of 10 offers at a time: price as the page shows it, condition, seller name and id, seller rating, ships-from and delivery estimate. Page 1 also carries the buy-box offer. Prices are pinned to a Canadian postal code.

### How do I automatically get Amazon.ca product offers from all sellers on amazon.ca?

Ask an AI agent connected to Reduck to run reduck/amazon.ca/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.ca/get-product-offers

### Is there a amazon.ca API to get Amazon.ca product offers from all sellers?

You do not need one. "Get Amazon.ca product offers from all sellers" drives the real amazon.ca pages in a browser, so it works whether or not amazon.ca offers an API for this.

### What information do I need to provide?

Required: asin. Optional: page, zipCode.

### What does it return?

It returns url, zip, asin, page, title, offers, total_offers, has_next_page.

### Do I need to be logged in to amazon.ca?

No. It only uses pages of amazon.ca that are reachable without signing in.

### Does it change anything on amazon.ca, or only read data?

It only reads. It looks things up on amazon.ca and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.ca/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.ca/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.ca/get-product-offers
