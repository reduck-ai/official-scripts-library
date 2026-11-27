# List Pelando hot deals

Automatically list Pelando hot deals on pelando.com.br. List the deals on the hottest tab of Pelando (Brazil's deal community), 20 at a time, hottest first, with the site's filters: period (today, this week or this month), hide expired deals, and stores. Each deal has its id, slug (the input of Get Pelando deal), link, title, type (promotion or coupon), temperature (the community vote score in degrees), price in reais, discount, free shipping, merchant and its id, the merchant link, image, who posted it, comment count, publication date, and whether it is expired. The fields have the same names as the Dealabs, mydealz and hotukdeals scripts; fields Pelando does not show in its lists (previous price, voucher code, category, description, start and end dates) are null. Pass next_cursor as cursor to get the next page. A period with no deal returns an empty list.

- Site: pelando.com.br
- Address: `reduck/pelando.com.br/list_hot_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pelando.com.br/list_hot_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pelando.com.br/list_hot_deals
```

## Input

- `cursor` (string | null, optional): next_cursor of the previous answer, for the next page. Null for the first page.
- `period` (string, optional): Period of the deals, as the site offers it: today (the last 24 hours, the site's default), week (since midnight 7 days ago) or month (since midnight 30 days ago).
- `store_ids` (array, optional): Only deals of these stores, by the merchant_id of deals from an earlier answer. Empty for all stores.
- `hide_expired` (boolean, optional): Leave out expired deals.

## Output

- `deals` (array, required)
- `period` (string, required)
- `next_cursor` (string | null, required): Pass as cursor for the next page. Null after the last page.
- `has_next_page` (boolean, required)

## FAQ

### What does "List Pelando hot deals" do?

List the deals on the hottest tab of Pelando (Brazil's deal community), 20 at a time, hottest first, with the site's filters: period (today, this week or this month), hide expired deals, and stores. Each deal has its id, slug (the input of Get Pelando deal), link, title, type (promotion or coupon), temperature (the community vote score in degrees), price in reais, discount, free shipping, merchant and its id, the merchant link, image, who posted it, comment count, publication date, and whether it is expired. The fields have the same names as the Dealabs, mydealz and hotukdeals scripts; fields Pelando does not show in its lists (previous price, voucher code, category, description, start and end dates) are null. Pass next_cursor as cursor to get the next page. A period with no deal returns an empty list.

### How do I automatically list Pelando hot deals on pelando.com.br?

Ask an AI agent connected to Reduck to run reduck/pelando.com.br/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pelando.com.br/list_hot_deals

### Is there a pelando.com.br API to list Pelando hot deals?

You do not need one. "List Pelando hot deals" drives the real pelando.com.br pages in a browser, so it works whether or not pelando.com.br offers an API for this.

### What information do I need to provide?

Optional: cursor, period, store_ids, hide_expired.

### What does it return?

It returns deals, period, next_cursor, has_next_page.

### Do I need to be logged in to pelando.com.br?

No. It only uses pages of pelando.com.br that are reachable without signing in.

### Does it change anything on pelando.com.br, or only read data?

It only reads. It looks things up on pelando.com.br and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pelando.com.br/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pelando.com.br/list_hot_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/pelando.com.br/list_hot_deals
