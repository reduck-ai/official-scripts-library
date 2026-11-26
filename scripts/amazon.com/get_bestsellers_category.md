# Get Amazon Bestsellers by Category

Automatically get Amazon Bestsellers by Category on amazon.com. Reads Amazon's Best Sellers list for a top-level category (rank, title, price, rating, review count). Prices are in the currency the store displays, returned as currency: US dollars unless the browser prefers another.

- Site: amazon.com
- Address: `reduck/amazon.com/get_bestsellers_category`
- Updated: 2026-11-25 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/get_bestsellers_category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/get_bestsellers_category
```

## Input

- `category` (string, required): The category's URL slug, e.g. "electronics", "books", "toys-and-games", "beauty", "software". Find the right slug by browsing amazon.com/Best-Sellers and reading it off the URL of the category tab you land on — it's the same slug Amazon's own nav uses.
- `limit` (integer, optional): Max products to return, in Amazon's own rank order. The list page renders 30 without scrolling; asking for more than that returns what the page holds.

## Output

- `category` (string, required)
- `currency` (string, required): ISO 4217 code of the currency of every price in this result, as the store displays it: the store's own (US dollars (USD)) unless the browser prefers another, which Amazon then shows instead.
- `products` (array, required)

## FAQ

### What does "Get Amazon Bestsellers by Category" do?

Reads Amazon's Best Sellers list for a top-level category (rank, title, price, rating, review count). Prices are in the currency the store displays, returned as currency: US dollars unless the browser prefers another.

### How do I automatically get Amazon Bestsellers by Category on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get_bestsellers_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get_bestsellers_category

### Is there a amazon.com API to get Amazon Bestsellers by Category?

You do not need one. "Get Amazon Bestsellers by Category" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Required: category. Optional: limit.

### What does it return?

It returns category, currency, products.

### Do I need to be logged in to amazon.com?

No. It only uses pages of amazon.com that are reachable without signing in.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get_bestsellers_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get_bestsellers_category

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/get_bestsellers_category
