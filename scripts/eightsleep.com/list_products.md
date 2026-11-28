# List Eight Sleep accessories catalogue

Automatically list Eight Sleep accessories catalogue on eightsleep.com. List the products on the Eight Sleep US accessories page, with each product's id, link, name, description, badge, default price and price before discount in US dollars, and its number of offers. Eight Sleep has no search box, so this script gives the full catalogue page. The Pod itself has its own page: pass pod-cover to eightsleep.com/get_product. Use a product id or link with eightsleep.com/get_product to get its sizes and offer ids.

- Site: eightsleep.com
- Address: `reduck/eightsleep.com/list_products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/eightsleep.com/list_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/list_products
```

## Input

It takes no input.

## Output

- `url` (string, required)
- `products` (array, required)
- `currency` (string | null, optional): Currency of the prices, e.g. usd.

## FAQ

### What does "List Eight Sleep accessories catalogue" do?

List the products on the Eight Sleep US accessories page, with each product's id, link, name, description, badge, default price and price before discount in US dollars, and its number of offers. Eight Sleep has no search box, so this script gives the full catalogue page. The Pod itself has its own page: pass pod-cover to eightsleep.com/get_product. Use a product id or link with eightsleep.com/get_product to get its sizes and offer ids.

### How do I automatically list Eight Sleep accessories catalogue on eightsleep.com?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/list_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/list_products

### Is there a eightsleep.com API to list Eight Sleep accessories catalogue?

You do not need one. "List Eight Sleep accessories catalogue" drives the real eightsleep.com pages in a browser, so it works whether or not eightsleep.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns url, currency, products.

### Do I need to be logged in to eightsleep.com?

No. It only uses pages of eightsleep.com that are reachable without signing in.

### Does it change anything on eightsleep.com, or only read data?

It only reads. It looks things up on eightsleep.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/list_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/list_products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/eightsleep.com/list_products
