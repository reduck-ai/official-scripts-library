# Get Amazon.co.uk product offers from all sellers

Automatically get Amazon.co.uk product offers from all sellers on amazon.co.uk. List every seller offering an Amazon.co.uk product, one page of 10 offers at a time: price as the store displays it, condition, seller name and id, seller rating, ships-from and delivery estimate. Page 1 also carries the buy-box offer. Prices are pinned to a UK postcode.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/get-product-offers`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get-product-offers
```

## Input

- `asin` (string, required): Amazon ASIN, as in /dp/<ASIN>.
- `page` (integer, optional): Page of the offer list, 10 offers each.
- `zipCode` (string, optional): UK postcode used to pin the store location.

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

### What does "Get Amazon.co.uk product offers from all sellers" do?

List every seller offering an Amazon.co.uk product, one page of 10 offers at a time: price as the store displays it, condition, seller name and id, seller rating, ships-from and delivery estimate. Page 1 also carries the buy-box offer. Prices are pinned to a UK postcode.

### How do I automatically get Amazon.co.uk product offers from all sellers on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get-product-offers

### Is there a amazon.co.uk API to get Amazon.co.uk product offers from all sellers?

You do not need one. "Get Amazon.co.uk product offers from all sellers" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Required: asin. Optional: page, zipCode.

### What does it return?

It returns url, zip, asin, page, title, offers, total_offers, has_next_page.

### Do I need to be logged in to amazon.co.uk?

No. It only uses pages of amazon.co.uk that are reachable without signing in.

### Does it change anything on amazon.co.uk, or only read data?

It only reads. It looks things up on amazon.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/get-product-offers
