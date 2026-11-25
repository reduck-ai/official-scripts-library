# List Amazon deals

Automatically list Amazon deals on amazon.com. List the deals on Amazon.com's deals page (Today's Deals, Black Friday), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price with their labels as Amazon writes them, the discount badge (for example "50% off"), the deal label (for example "Black Friday Deal", or "Ends in" before a countdown) and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page (Lightning deals, Doorbusters, Top 100+…) by the id from tabs, refinements as group:value taken from refinements (department, brand, customer reviews, Prime programs), a discount range in percent and a price range. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. Tabs and filters change with Amazon's events. A product without a deal of its own can appear in the grid; its deal fields are null.

- Site: amazon.com
- Address: `reduck/amazon.com/list_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/list_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/list_deals
```

## Input

- `tab` (string, optional): A tab of the deals page, by its id from tabs (for example deal-collection-lightning). Omit for the page's default view.
- `cursor` (integer, optional): next_cursor of the previous page; 0 for the first.
- `zipCode` (string, optional): US ZIP code prices and availability are shown for. Default 10001.
- `maxPrice` (number, optional): Maximum deal price, in dollars.
- `minPrice` (number, optional): Minimum deal price, in dollars.
- `maxDiscount` (integer, optional): Maximum discount in percent.
- `minDiscount` (integer, optional): Minimum discount in percent.
- `refinements` (array, optional): Filters as group:value, taken from refinements of an earlier call: departments:<id>, brands:<id|name>, reviewRating:4, accessType:<id>. Values of one group are combined as the page does.

## Output

- `url` (string, required)
- `tabs` (array, required)
- `deals` (array, required)
- `next_cursor` (integer | null, required)
- `refinements` (array, required)
- `tab` (string | null, optional)

## FAQ

### What does "List Amazon deals" do?

List the deals on Amazon.com's deals page (Today's Deals, Black Friday), one page of 30 at a time: each deal's ASIN, title, URL, image, deal price and list price with their labels as Amazon writes them, the discount badge (for example "50% off"), the deal label (for example "Black Friday Deal", or "Ends in" before a countdown) and its end time, deal id, type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL) and state, percent claimed for lightning deals, rating, review count and brand. Optional: a tab of the page (Lightning deals, Doorbusters, Top 100+…) by the id from tabs, refinements as group:value taken from refinements (department, brand, customer reviews, Prime programs), a discount range in percent and a price range. Returns the store's tabs and the refinements available for this view. Pass next_cursor back as cursor for the next page; it is null when the page is empty. A filter the page does not offer is refused, not ignored. Tabs and filters change with Amazon's events. A product without a deal of its own can appear in the grid; its deal fields are null.

### How do I automatically list Amazon deals on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/list_deals

### Is there a amazon.com API to list Amazon deals?

You do not need one. "List Amazon deals" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Optional: tab, cursor, zipCode, maxPrice, minPrice, maxDiscount, minDiscount, refinements.

### What does it return?

It returns tab, url, tabs, deals, next_cursor, refinements.

### Do I need to be logged in to amazon.com?

No. It only uses pages of amazon.com that are reachable without signing in.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/list_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/list_deals
