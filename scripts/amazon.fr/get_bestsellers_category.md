# Get Amazon.fr Bestsellers by Category

Automatically get Amazon.fr Bestsellers by Category on amazon.fr. Reads Amazon.fr's Best Sellers list for a top-level category (rank, title, price, rating, review count). Prices are in the currency the store displays, returned as currency: euros unless the browser prefers another.

- Site: amazon.fr
- Address: `reduck/amazon.fr/get_bestsellers_category`
- Updated: 2026-11-25 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/get_bestsellers_category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/get_bestsellers_category
```

## Input

- `category` (string, required): The category's URL slug, e.g. "books" or "toys". Read it off the URL of a category tab at amazon.fr/gp/bestsellers: slugs are this store's own, so one from another Amazon store may not exist here.
- `limit` (integer, optional): Max products to return, in Amazon's own rank order. The list page renders 30 without scrolling; asking for more than that returns what the page holds.

## Output

- `category` (string, required)
- `currency` (string, required): ISO 4217 code of the currency of every price in this result, as the store displays it: the store's own (euros (EUR)) unless the browser prefers another, which Amazon then shows instead.
- `products` (array, required)

## FAQ

### What does "Get Amazon.fr Bestsellers by Category" do?

Reads Amazon.fr's Best Sellers list for a top-level category (rank, title, price, rating, review count). Prices are in the currency the store displays, returned as currency: euros unless the browser prefers another.

### How do I automatically get Amazon.fr Bestsellers by Category on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/get_bestsellers_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/get_bestsellers_category

### Is there a amazon.fr API to get Amazon.fr Bestsellers by Category?

You do not need one. "Get Amazon.fr Bestsellers by Category" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Required: category. Optional: limit.

### What does it return?

It returns category, currency, products.

### Do I need to be logged in to amazon.fr?

No. It only uses pages of amazon.fr that are reachable without signing in.

### Does it change anything on amazon.fr, or only read data?

It only reads. It looks things up on amazon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/get_bestsellers_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/get_bestsellers_category

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/get_bestsellers_category
