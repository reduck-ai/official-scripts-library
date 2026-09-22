# Get Capterra Product Reviews

Automatically get Capterra Product Reviews on capterra.com. Reads a public Capterra product's reviews (reviewer, overall rating, pros, cons, date).

- Site: capterra.com
- Address: `reduck/capterra.com/get_product_reviews`
- Updated: 2026-08-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/capterra.com/get_product_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/capterra.com/get_product_reviews
```

## Input

- `productUrl` (string, required): The product's Capterra page URL, e.g. https://www.capterra.com/p/135003/Slack/ (with or without a trailing /reviews/). Find it by searching the product on capterra.com and copying its page URL — the numeric id in the URL isn't something you can construct from the product name alone.
- `limit` (integer, optional): Max reviews to return, in the order the page renders them (Capterra's default "Most Helpful" sort). The page loads a first batch without scrolling; asking for more than that returns what the page holds.

## Output

- `reviews` (array, required)
- `product_url` (string, required)

## FAQ

### What does "Get Capterra Product Reviews" do?

Reads a public Capterra product's reviews (reviewer, overall rating, pros, cons, date).

### How do I automatically get Capterra Product Reviews on capterra.com?

Ask an AI agent connected to Reduck to run reduck/capterra.com/get_product_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/capterra.com/get_product_reviews

### Is there a capterra.com API to get Capterra Product Reviews?

You do not need one. "Get Capterra Product Reviews" drives the real capterra.com pages in a browser, so it works whether or not capterra.com offers an API for this.

### What information do I need to provide?

Required: productUrl. Optional: limit.

### What does it return?

It returns reviews, product_url.

### Do I need to be logged in to capterra.com?

No. It only uses pages of capterra.com that are reachable without signing in.

### Does it change anything on capterra.com, or only read data?

It only reads. It looks things up on capterra.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/capterra.com/get_product_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/capterra.com/get_product_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/capterra.com/get_product_reviews
