# Get Amazon.es bestsellers by category

Automatically get Amazon.es bestsellers by category on amazon.es. Read Amazon.es's Best Sellers list for a top-level category: rank, ASIN, title, price in euros, rating and review count. Pass the category's URL slug, as it appears on amazon.es/gp/bestsellers.

- Site: amazon.es
- Address: `reduck/amazon.es/get_bestsellers_category`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/get_bestsellers_category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/get_bestsellers_category
```

## Input

- `category` (string, required): The category's URL slug, for example electronics or books, as shown in the Best Sellers URL.
- `limit` (integer, optional): Max products to return, in Amazon's rank order. The page renders 30 without scrolling.

## Output

- `category` (string, required)
- `products` (array, required)

## FAQ

### What does "Get Amazon.es bestsellers by category" do?

Read Amazon.es's Best Sellers list for a top-level category: rank, ASIN, title, price in euros, rating and review count. Pass the category's URL slug, as it appears on amazon.es/gp/bestsellers.

### How do I automatically get Amazon.es bestsellers by category on amazon.es?

Ask an AI agent connected to Reduck to run reduck/amazon.es/get_bestsellers_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/get_bestsellers_category

### Is there a amazon.es API to get Amazon.es bestsellers by category?

You do not need one. "Get Amazon.es bestsellers by category" drives the real amazon.es pages in a browser, so it works whether or not amazon.es offers an API for this.

### What information do I need to provide?

Required: category. Optional: limit.

### What does it return?

It returns category, products.

### Do I need to be logged in to amazon.es?

No. It only uses pages of amazon.es that are reachable without signing in.

### Does it change anything on amazon.es, or only read data?

It only reads. It looks things up on amazon.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/get_bestsellers_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/get_bestsellers_category

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/get_bestsellers_category
