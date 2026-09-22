# Get G2 product reviews

Automatically get G2 product reviews on g2.com. Fetch reviews for a G2 product from its Reviews page: reviewer name, role, rating, date, title, and the like/dislike/problems-solved answer sections. No login required.

- Site: g2.com
- Address: `reduck/g2.com/get_product_reviews`
- Updated: 2026-09-02 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/g2.com/get_product_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/g2.com/get_product_reviews
```

## Input

- `product_slug` (string, required): G2 product URL slug, e.g. "slack" (from g2.com/products/<slug>/reviews)

## Output

- `reviews` (array, required)
- `product_slug` (string, required)

## FAQ

### What does "Get G2 product reviews" do?

Fetch reviews for a G2 product from its Reviews page: reviewer name, role, rating, date, title, and the like/dislike/problems-solved answer sections. No login required.

### How do I automatically get G2 product reviews on g2.com?

Ask an AI agent connected to Reduck to run reduck/g2.com/get_product_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/get_product_reviews

### Is there a g2.com API to get G2 product reviews?

You do not need one. "Get G2 product reviews" drives the real g2.com pages in a browser, so it works whether or not g2.com offers an API for this.

### What information do I need to provide?

Required: product_slug.

### What does it return?

It returns reviews, product_slug.

### Do I need to be logged in to g2.com?

No. It only uses pages of g2.com that are reachable without signing in.

### Does it change anything on g2.com, or only read data?

It only reads. It looks things up on g2.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/g2.com/get_product_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/get_product_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/g2.com/get_product_reviews
