# Get G2 product profile

Automatically get G2 product profile on g2.com. Fetch a G2 product's profile by slug: vendor, star rating, review count, pricing tier names, and pros/cons themes with mention counts drawn from real user reviews.

- Site: g2.com
- Address: `reduck/g2.com/get_product`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/g2.com/get_product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/g2.com/get_product
```

## Input

- `slug` (string, required): G2 product slug, e.g. 'jira' or 'notion' (from search_products)

## Output

- `url` (string, optional)
- `cons` (array, optional)
- `name` (string | null, optional)
- `pros` (array, optional)
- `slug` (string, optional)
- `found` (boolean, optional): false when the product slug does not exist on G2 (404)
- `rating` (number | null, optional)
- `vendor` (string | null, optional)
- `vendor_url` (string | null, optional)
- `review_count` (integer | null, optional)
- `pricing_tiers` (array, optional)

## FAQ

### What does "Get G2 product profile" do?

Fetch a G2 product's profile by slug: vendor, star rating, review count, pricing tier names, and pros/cons themes with mention counts drawn from real user reviews.

### How do I automatically get G2 product profile on g2.com?

Ask an AI agent connected to Reduck to run reduck/g2.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/get_product

### Is there a g2.com API to get G2 product profile?

You do not need one. "Get G2 product profile" drives the real g2.com pages in a browser, so it works whether or not g2.com offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns url, cons, name, pros, slug, found, rating, vendor, vendor_url, review_count, pricing_tiers.

### Do I need to be logged in to g2.com?

No. It only uses pages of g2.com that are reachable without signing in.

### Does it change anything on g2.com, or only read data?

It only reads. It looks things up on g2.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/g2.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/get_product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/g2.com/get_product
