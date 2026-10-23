# List Amazon category page

Automatically list Amazon category page on amazon.com. List one page of an Amazon search or category listing, every product card in page order. Takes the listing's link as you see it on Amazon after a search or a category click. Returns the link, the heading, and the products (ASIN, position on the page, and whether the card is sponsored). A product can appear twice, once as a sponsored card and once as a regular result. Only the ASINs are returned; pass them to Get Amazon product for the details.

- Site: amazon.com
- Address: `reduck/amazon.com/list-category`
- Updated: 2026-10-22 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/list-category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/list-category
```

## Input

- `url` (string, required)
- `zipCode` (string, optional): US ZIP for delivery location. Default 10001 (New York, NY).

## Output

- `url` (string, required)
- `products` (array, required)
- `heading` (string | null, optional)

## FAQ

### What does "List Amazon category page" do?

List one page of an Amazon search or category listing, every product card in page order. Takes the listing's link as you see it on Amazon after a search or a category click. Returns the link, the heading, and the products (ASIN, position on the page, and whether the card is sponsored). A product can appear twice, once as a sponsored card and once as a regular result. Only the ASINs are returned; pass them to Get Amazon product for the details.

### How do I automatically list Amazon category page on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/list-category

### Is there a amazon.com API to list Amazon category page?

You do not need one. "List Amazon category page" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: zipCode.

### What does it return?

It returns url, heading, products.

### Do I need to be logged in to amazon.com?

No. It only uses pages of amazon.com that are reachable without signing in.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/list-category

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/list-category
