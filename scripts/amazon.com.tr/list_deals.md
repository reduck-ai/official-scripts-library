# List Amazon.com.tr deals

Automatically list Amazon.com.tr deals on amazon.com.tr. List the deals on Amazon.com.tr's deals page (fırsatlar, Black Friday), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price with their labels as Amazon writes them and the currency the page shows, the discount badge, the deal label as Amazon writes it and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page by the id from tabs, refinements as group:value taken from refinements, a discount range in percent and a price range, when the page offers them. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. A product without a deal of its own can appear in the grid; its deal fields are null.

- Site: amazon.com.tr
- Address: `reduck/amazon.com.tr/list_deals`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.tr/list_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.tr/list_deals
```

## Input

- `tab` (string, optional): A tab of the deals page, by its id from tabs. Omit for the page's default view.
- `cursor` (integer, optional): next_cursor of the previous page; 0 for the first.
- `maxPrice` (number, optional): Maximum deal price, in Turkish lira. Amazon offers this filter only while the page shows prices in the store's own currency; otherwise the run is refused and names the filters the page offers.
- `minPrice` (number, optional): Minimum deal price, in Turkish lira. Amazon offers this filter only while the page shows prices in the store's own currency; otherwise the run is refused and names the filters the page offers.
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

### What does "List Amazon.com.tr deals" do?

List the deals on Amazon.com.tr's deals page (fırsatlar, Black Friday), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price with their labels as Amazon writes them and the currency the page shows, the discount badge, the deal label as Amazon writes it and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page by the id from tabs, refinements as group:value taken from refinements, a discount range in percent and a price range, when the page offers them. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. A product without a deal of its own can appear in the grid; its deal fields are null.

### How do I automatically list Amazon.com.tr deals on amazon.com.tr?

Ask an AI agent connected to Reduck to run reduck/amazon.com.tr/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.tr/list_deals

### Is there a amazon.com.tr API to list Amazon.com.tr deals?

You do not need one. "List Amazon.com.tr deals" drives the real amazon.com.tr pages in a browser, so it works whether or not amazon.com.tr offers an API for this.

### What information do I need to provide?

Optional: tab, cursor, maxPrice, minPrice, maxDiscount, minDiscount, refinements.

### What does it return?

It returns tab, url, tabs, deals, next_cursor, refinements.

### Do I need to be logged in to amazon.com.tr?

No. It only uses pages of amazon.com.tr that are reachable without signing in.

### Does it change anything on amazon.com.tr, or only read data?

It only reads. It looks things up on amazon.com.tr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.tr/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.tr/list_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.tr/list_deals
