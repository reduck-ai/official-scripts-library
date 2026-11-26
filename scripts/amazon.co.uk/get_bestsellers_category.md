# Get Amazon.co.uk bestsellers by category

Automatically get Amazon.co.uk bestsellers by category on amazon.co.uk. Read Amazon.co.uk's Best Sellers list for a top-level category: rank, ASIN, title, price, rating and review count. Prices are in the currency the store displays, returned as currency: pounds sterling unless the browser prefers another. Pass the category's URL slug, as it appears in the Best Sellers URL.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/get_bestsellers_category`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/get_bestsellers_category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get_bestsellers_category
```

## Input

- `category` (string, required): The category's URL slug, for example electronics or books, as shown in the Best Sellers URL.
- `limit` (integer, optional): Max products to return, in Amazon's rank order. The page renders 30 without scrolling.

## Output

- `category` (string, required)
- `currency` (string, required): ISO 4217 code of the currency of every price in this result, as the store displays it: the store's own (pounds sterling (GBP)) unless the browser prefers another, which Amazon then shows instead.
- `products` (array, required)

## FAQ

### What does "Get Amazon.co.uk bestsellers by category" do?

Read Amazon.co.uk's Best Sellers list for a top-level category: rank, ASIN, title, price, rating and review count. Prices are in the currency the store displays, returned as currency: pounds sterling unless the browser prefers another. Pass the category's URL slug, as it appears in the Best Sellers URL.

### How do I automatically get Amazon.co.uk bestsellers by category on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/get_bestsellers_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get_bestsellers_category

### Is there a amazon.co.uk API to get Amazon.co.uk bestsellers by category?

You do not need one. "Get Amazon.co.uk bestsellers by category" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Required: category. Optional: limit.

### What does it return?

It returns category, currency, products.

### Do I need to be logged in to amazon.co.uk?

No. It only uses pages of amazon.co.uk that are reachable without signing in.

### Does it change anything on amazon.co.uk, or only read data?

It only reads. It looks things up on amazon.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/get_bestsellers_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get_bestsellers_category

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/get_bestsellers_category
