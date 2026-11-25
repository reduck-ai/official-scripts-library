# Search hotukdeals deals

Automatically search hotukdeals deals on hotukdeals.com. Search the deals and vouchers posted on hotukdeals (the UK's deal community) by keyword, with the site's own filters: sort order, hide expired or local offers, price range, minimum temperature (the community vote) and period. Returns one page of 30 results with the page count. Each deal has its id, link, title, type, temperature, price and previous price in pounds sterling, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Without a period, hotukdeals searches the last year. A search with no match returns an empty list.

- Site: hotukdeals.com
- Address: `reduck/hotukdeals.com/search_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hotukdeals.com/search_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hotukdeals.com/search_deals
```

## Input

- `query` (string, required): Words to search for, for example "airfryer" or "ps5".
- `page` (integer, optional)
- `sort` (string, optional): relevance (the site's default), new (newest first), temp (hottest first), highest_price, lowest_price, or discussion (recently commented).
- `period` (string, optional): How far back to search. hotukdeals searches the last year when this is not given.
- `price_to` (number, optional): Highest price in pounds sterling.
- `hide_local` (boolean, optional): Leave out offers valid only in some shops or regions.
- `price_from` (number, optional): Lowest price in pounds sterling.
- `hide_expired` (boolean, optional)
- `temperature_from` (integer, optional): Only deals at this temperature or more, for example 100.

## Output

- `page` (integer, required)
- `deals` (array, required)
- `query` (string, required)
- `last_page` (integer | null, optional)

## FAQ

### What does "Search hotukdeals deals" do?

Search the deals and vouchers posted on hotukdeals (the UK's deal community) by keyword, with the site's own filters: sort order, hide expired or local offers, price range, minimum temperature (the community vote) and period. Returns one page of 30 results with the page count. Each deal has its id, link, title, type, temperature, price and previous price in pounds sterling, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Without a period, hotukdeals searches the last year. A search with no match returns an empty list.

### How do I automatically search hotukdeals deals on hotukdeals.com?

Ask an AI agent connected to Reduck to run reduck/hotukdeals.com/search_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hotukdeals.com/search_deals

### Is there a hotukdeals.com API to search hotukdeals deals?

You do not need one. "Search hotukdeals deals" drives the real hotukdeals.com pages in a browser, so it works whether or not hotukdeals.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, period, price_to, hide_local, price_from, hide_expired, temperature_from.

### What does it return?

It returns page, deals, query, last_page.

### Do I need to be logged in to hotukdeals.com?

No. It only uses pages of hotukdeals.com that are reachable without signing in.

### Does it change anything on hotukdeals.com, or only read data?

It only reads. It looks things up on hotukdeals.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hotukdeals.com/search_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hotukdeals.com/search_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hotukdeals.com/search_deals
