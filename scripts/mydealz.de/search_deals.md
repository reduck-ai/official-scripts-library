# Search mydealz deals

Automatically search mydealz deals on mydealz.de. Search the deals and vouchers posted on mydealz (Germany's deal community) by keyword, with the site's own filters: sort order, hide expired or local offers, price range, minimum temperature (the community vote) and period. Returns one page of 30 results with the page count. Each deal has its id, link, title, type, temperature, price and previous price in euros, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Without a period, mydealz searches the last year. A search with no match returns an empty list.

- Site: mydealz.de
- Address: `reduck/mydealz.de/search_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mydealz.de/search_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mydealz.de/search_deals
```

## Input

- `query` (string, required): Words to search for, for example "airfryer" or "ps5".
- `page` (integer, optional)
- `sort` (string, optional): relevance (the site's default), new (newest first), temp (hottest first), highest_price, lowest_price, or discussion (recently commented).
- `period` (string, optional): How far back to search. mydealz searches the last year when this is not given.
- `price_to` (number, optional): Highest price in euros.
- `hide_local` (boolean, optional): Leave out offers valid only in some shops or regions.
- `price_from` (number, optional): Lowest price in euros.
- `hide_expired` (boolean, optional)
- `temperature_from` (integer, optional): Only deals at this temperature or more, for example 100.

## Output

- `page` (integer, required)
- `deals` (array, required)
- `query` (string, required)
- `last_page` (integer | null, optional)

## FAQ

### What does "Search mydealz deals" do?

Search the deals and vouchers posted on mydealz (Germany's deal community) by keyword, with the site's own filters: sort order, hide expired or local offers, price range, minimum temperature (the community vote) and period. Returns one page of 30 results with the page count. Each deal has its id, link, title, type, temperature, price and previous price in euros, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Without a period, mydealz searches the last year. A search with no match returns an empty list.

### How do I automatically search mydealz deals on mydealz.de?

Ask an AI agent connected to Reduck to run reduck/mydealz.de/search_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mydealz.de/search_deals

### Is there a mydealz.de API to search mydealz deals?

You do not need one. "Search mydealz deals" drives the real mydealz.de pages in a browser, so it works whether or not mydealz.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, period, price_to, hide_local, price_from, hide_expired, temperature_from.

### What does it return?

It returns page, deals, query, last_page.

### Do I need to be logged in to mydealz.de?

No. It only uses pages of mydealz.de that are reachable without signing in.

### Does it change anything on mydealz.de, or only read data?

It only reads. It looks things up on mydealz.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mydealz.de/search_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mydealz.de/search_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mydealz.de/search_deals
