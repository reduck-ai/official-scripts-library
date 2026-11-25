# List Amazon.se deals

Automatically list Amazon.se deals on amazon.se. List the deals on Amazon.se's deals page (erbjudanden, Black Friday), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price in Swedish kronor with their labels as Amazon writes them, the discount badge, the deal label as Amazon writes it and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page by the id from tabs, refinements as group:value taken from refinements, a discount range in percent and a price range, when the page offers them. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. A product without a deal of its own can appear in the grid; its deal fields are null.

- Site: amazon.se
- Address: `reduck/amazon.se/list_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.se/list_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.se/list_deals
```

## Input

- `tab` (string, optional): A tab of the deals page, by its id from tabs. Omit for the page's default view.
- `cursor` (integer, optional): next_cursor of the previous page; 0 for the first.
- `maxPrice` (number, optional): Maximum deal price, in Swedish kronor.
- `minPrice` (number, optional): Minimum deal price, in Swedish kronor.
- `maxDiscount` (integer, optional): Maximum discount in percent, when the page offers a discount filter.
- `minDiscount` (integer, optional): Minimum discount in percent, when the page offers a discount filter.
- `refinements` (array, optional): Filters as group:value, taken from refinements of an earlier call.

## Output

- `url` (string, required)
- `tabs` (array, required)
- `deals` (array, required)
- `next_cursor` (integer | null, required)
- `refinements` (array, required)
- `tab` (string | null, optional)

## FAQ

### What does "List Amazon.se deals" do?

List the deals on Amazon.se's deals page (erbjudanden, Black Friday), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price in Swedish kronor with their labels as Amazon writes them, the discount badge, the deal label as Amazon writes it and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page by the id from tabs, refinements as group:value taken from refinements, a discount range in percent and a price range, when the page offers them. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. A product without a deal of its own can appear in the grid; its deal fields are null.

### How do I automatically list Amazon.se deals on amazon.se?

Ask an AI agent connected to Reduck to run reduck/amazon.se/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.se/list_deals

### Is there a amazon.se API to list Amazon.se deals?

You do not need one. "List Amazon.se deals" drives the real amazon.se pages in a browser, so it works whether or not amazon.se offers an API for this.

### What information do I need to provide?

Optional: tab, cursor, maxPrice, minPrice, maxDiscount, minDiscount, refinements.

### What does it return?

It returns tab, url, tabs, deals, next_cursor, refinements.

### Do I need to be logged in to amazon.se?

No. It only uses pages of amazon.se that are reachable without signing in.

### Does it change anything on amazon.se, or only read data?

It only reads. It looks things up on amazon.se and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.se/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.se/list_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.se/list_deals
