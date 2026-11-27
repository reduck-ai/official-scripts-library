# Search Pelando deals

Automatically search Pelando deals on pelando.com.br. Search the deals and coupons posted on Pelando (Brazil's deal community) by keyword, with the site's own filters: sort order (newest, hottest or recently commented) and hide expired deals. Returns 20 results at a time. Each deal has its id, slug (the input of Get Pelando deal), link, title, type (promotion or coupon), temperature (the community vote score in degrees), price in reais, discount, free shipping, merchant and its id, the merchant link, image, who posted it, comment count, publication date, and whether it is expired. The fields have the same names as the Dealabs, mydealz and hotukdeals scripts; fields Pelando does not show in its lists (previous price, voucher code, category, description, start and end dates) are null. Pass next_cursor as cursor to get the next page. A search with no match returns an empty list.

- Site: pelando.com.br
- Address: `reduck/pelando.com.br/search_deals`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pelando.com.br/search_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pelando.com.br/search_deals
```

## Input

- `query` (string, required): Words to search for, for example "airfryer" or "iphone 15".
- `sort` (string, optional): new (newest first, the site's default), hot (highest temperature first) or commented (recently commented first).
- `cursor` (string | null, optional): next_cursor of the previous answer, for the next page. Null for the first page.
- `hide_expired` (boolean, optional): Leave out expired deals.

## Output

- `deals` (array, required)
- `query` (string, required)
- `next_cursor` (string | null, required): Pass as cursor for the next page. Null after the last page.
- `has_next_page` (boolean, required)

## FAQ

### What does "Search Pelando deals" do?

Search the deals and coupons posted on Pelando (Brazil's deal community) by keyword, with the site's own filters: sort order (newest, hottest or recently commented) and hide expired deals. Returns 20 results at a time. Each deal has its id, slug (the input of Get Pelando deal), link, title, type (promotion or coupon), temperature (the community vote score in degrees), price in reais, discount, free shipping, merchant and its id, the merchant link, image, who posted it, comment count, publication date, and whether it is expired. The fields have the same names as the Dealabs, mydealz and hotukdeals scripts; fields Pelando does not show in its lists (previous price, voucher code, category, description, start and end dates) are null. Pass next_cursor as cursor to get the next page. A search with no match returns an empty list.

### How do I automatically search Pelando deals on pelando.com.br?

Ask an AI agent connected to Reduck to run reduck/pelando.com.br/search_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pelando.com.br/search_deals

### Is there a pelando.com.br API to search Pelando deals?

You do not need one. "Search Pelando deals" drives the real pelando.com.br pages in a browser, so it works whether or not pelando.com.br offers an API for this.

### What information do I need to provide?

Required: query. Optional: sort, cursor, hide_expired.

### What does it return?

It returns deals, query, next_cursor, has_next_page.

### Do I need to be logged in to pelando.com.br?

No. It only uses pages of pelando.com.br that are reachable without signing in.

### Does it change anything on pelando.com.br, or only read data?

It only reads. It looks things up on pelando.com.br and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pelando.com.br/search_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pelando.com.br/search_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/pelando.com.br/search_deals
