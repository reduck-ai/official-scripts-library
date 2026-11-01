# List Amazon.fr category page

Automatically list Amazon.fr category page on amazon.fr. List one page of an Amazon.fr search or category listing, every product card in page order. Takes the listing's link as you see it on Amazon after a search or a category click. Returns the link, the heading, and the products (ASIN, position on the page, and whether the card is sponsored). A product can appear twice, once as a sponsored card and once as a regular result. Only the ASINs are returned; pass them to Get Amazon product for the details.

- Site: amazon.fr
- Address: `reduck/amazon.fr/list-category`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/list-category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list-category
```

## Input

- `url` (string, required)
- `zipCode` (string, optional): French postcode for delivery location. Default 75001 (Paris 1er).

## Output

- `url` (string, required)
- `products` (array, required)
- `heading` (string | null, optional)

## FAQ

### What does "List Amazon.fr category page" do?

List one page of an Amazon.fr search or category listing, every product card in page order. Takes the listing's link as you see it on Amazon after a search or a category click. Returns the link, the heading, and the products (ASIN, position on the page, and whether the card is sponsored). A product can appear twice, once as a sponsored card and once as a regular result. Only the ASINs are returned; pass them to Get Amazon product for the details.

### How do I automatically list Amazon.fr category page on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list-category

### Is there a amazon.fr API to list Amazon.fr category page?

You do not need one. "List Amazon.fr category page" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Required: url. Optional: zipCode.

### What does it return?

It returns url, heading, products.

### Do I need to be logged in to amazon.fr?

No. It only uses pages of amazon.fr that are reachable without signing in.

### Does it change anything on amazon.fr, or only read data?

It only reads. It looks things up on amazon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list-category

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/list-category
