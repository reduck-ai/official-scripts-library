# List Amazon.com.mx deals

Automatically list Amazon.com.mx deals on amazon.com.mx. List the deals on Amazon.com.mx's deals page (Promociones, Buen Fin, Black Friday), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price in Mexican pesos with their labels as Amazon writes them, the discount badge, the deal label as Amazon writes it and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page by the id from tabs, refinements as group:value taken from refinements, a discount range in percent and a price range, when the page offers them. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. A product without a deal of its own can appear in the grid; its deal fields are null.

- Site: amazon.com.mx
- Address: `reduck/amazon.com.mx/list_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.mx/list_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.mx/list_deals
```

## Input

- `tab` (string, optional): A tab of the deals page, by its id from tabs. Omit for the page's default view.
- `cursor` (integer, optional): next_cursor of the previous page; 0 for the first.
- `maxPrice` (number, optional): Maximum deal price, in Mexican pesos.
- `minPrice` (number, optional): Minimum deal price, in Mexican pesos.
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

### What does "List Amazon.com.mx deals" do?

List the deals on Amazon.com.mx's deals page (Promociones, Buen Fin, Black Friday), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price in Mexican pesos with their labels as Amazon writes them, the discount badge, the deal label as Amazon writes it and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page by the id from tabs, refinements as group:value taken from refinements, a discount range in percent and a price range, when the page offers them. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. A product without a deal of its own can appear in the grid; its deal fields are null.

### How do I automatically list Amazon.com.mx deals on amazon.com.mx?

Ask an AI agent connected to Reduck to run reduck/amazon.com.mx/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.mx/list_deals

### Is there a amazon.com.mx API to list Amazon.com.mx deals?

You do not need one. "List Amazon.com.mx deals" drives the real amazon.com.mx pages in a browser, so it works whether or not amazon.com.mx offers an API for this.

### What information do I need to provide?

Optional: tab, cursor, maxPrice, minPrice, maxDiscount, minDiscount, refinements.

### What does it return?

It returns tab, url, tabs, deals, next_cursor, refinements.

### Do I need to be logged in to amazon.com.mx?

No. It only uses pages of amazon.com.mx that are reachable without signing in.

### Does it change anything on amazon.com.mx, or only read data?

It only reads. It looks things up on amazon.com.mx and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.mx/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.mx/list_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.mx/list_deals
