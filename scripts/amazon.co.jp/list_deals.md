# List Amazon.co.jp deals

Automatically list Amazon.co.jp deals on amazon.co.jp. List the deals on Amazon.co.jp's deals page (タイムセール), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price with their labels as Amazon writes them and the currency the page shows, the discount badge, the deal label as Amazon writes it and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page by the id from tabs, refinements as group:value taken from refinements, a discount range in percent and a price range, when the page offers them. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. Tabs and filters change with Amazon's events. A product without a deal of its own can appear in the grid; its deal fields are null.

- Site: amazon.co.jp
- Address: `reduck/amazon.co.jp/list_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.jp/list_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.jp/list_deals
```

## Input

- `tab` (string, optional): A tab of the deals page, by its id from tabs. Omit for the page's default view.
- `cursor` (integer, optional): next_cursor of the previous page; 0 for the first.
- `maxPrice` (number, optional): Maximum deal price, in the currency the page shows.
- `minPrice` (number, optional): Minimum deal price, in the currency the page shows.
- `maxDiscount` (integer, optional): Maximum discount in percent, when the page offers a discount filter.
- `minDiscount` (integer, optional): Minimum discount in percent, when the page offers a discount filter.
- `refinements` (array, optional): Filters as group:value, taken from refinements of an earlier call (departments, brands, reviewRating, accessType…).

## Output

- `url` (string, required)
- `tabs` (array, required)
- `deals` (array, required)
- `next_cursor` (integer | null, required)
- `refinements` (array, required)
- `tab` (string | null, optional)

## FAQ

### What does "List Amazon.co.jp deals" do?

List the deals on Amazon.co.jp's deals page (タイムセール), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price with their labels as Amazon writes them and the currency the page shows, the discount badge, the deal label as Amazon writes it and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page by the id from tabs, refinements as group:value taken from refinements, a discount range in percent and a price range, when the page offers them. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. Tabs and filters change with Amazon's events. A product without a deal of its own can appear in the grid; its deal fields are null.

### How do I automatically list Amazon.co.jp deals on amazon.co.jp?

Ask an AI agent connected to Reduck to run reduck/amazon.co.jp/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.jp/list_deals

### Is there a amazon.co.jp API to list Amazon.co.jp deals?

You do not need one. "List Amazon.co.jp deals" drives the real amazon.co.jp pages in a browser, so it works whether or not amazon.co.jp offers an API for this.

### What information do I need to provide?

Optional: tab, cursor, maxPrice, minPrice, maxDiscount, minDiscount, refinements.

### What does it return?

It returns tab, url, tabs, deals, next_cursor, refinements.

### Do I need to be logged in to amazon.co.jp?

No. It only uses pages of amazon.co.jp that are reachable without signing in.

### Does it change anything on amazon.co.jp, or only read data?

It only reads. It looks things up on amazon.co.jp and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.jp/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.jp/list_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.jp/list_deals
