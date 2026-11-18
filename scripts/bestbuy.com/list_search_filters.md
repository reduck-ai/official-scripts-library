# List Best Buy search filters

Automatically list Best Buy search filters on bestbuy.com. List the filters Best Buy offers for a product search: the sort orders, and every left-column filter for this query (category, sold and shipped by Best Buy, brand, condition, customer rating, price bands, deals, availability and the product's own attributes such as color or connection type), each value with its count and the refinement string Search Best Buy products takes. Filters depend on the query and on the category Best Buy narrows it to, so ask for the search you will run, with the same all_categories.

- Site: bestbuy.com
- Address: `reduck/bestbuy.com/list_search_filters`
- Updated: 2026-11-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bestbuy.com/list_search_filters`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/list_search_filters
```

## Input

- `query` (string, required): Free-text search query.
- `all_categories` (boolean, optional): Same meaning as in Search Best Buy products: true lists the filters of a search in every category.

## Output

- `query` (string, required)
- `sorts` (array, required)
- `filters` (array, required)
- `category` (string | null, required): The category Best Buy narrowed the search to, null when it searched all categories.
- `total_results` (integer, required)

## FAQ

### What does "List Best Buy search filters" do?

List the filters Best Buy offers for a product search: the sort orders, and every left-column filter for this query (category, sold and shipped by Best Buy, brand, condition, customer rating, price bands, deals, availability and the product's own attributes such as color or connection type), each value with its count and the refinement string Search Best Buy products takes. Filters depend on the query and on the category Best Buy narrows it to, so ask for the search you will run, with the same all_categories.

### How do I automatically list Best Buy search filters on bestbuy.com?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/list_search_filters

### Is there a bestbuy.com API to list Best Buy search filters?

You do not need one. "List Best Buy search filters" drives the real bestbuy.com pages in a browser, so it works whether or not bestbuy.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: all_categories.

### What does it return?

It returns query, sorts, filters, category, total_results.

### Do I need to be logged in to bestbuy.com?

No. It only uses pages of bestbuy.com that are reachable without signing in.

### Does it change anything on bestbuy.com, or only read data?

It only reads. It looks things up on bestbuy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/list_search_filters

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bestbuy.com/list_search_filters
