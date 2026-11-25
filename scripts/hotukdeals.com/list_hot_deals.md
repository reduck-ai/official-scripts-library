# List hotukdeals hot deals

Automatically list hotukdeals hot deals on hotukdeals.com. List the deals on the hot tab of hotukdeals (the UK's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in pounds sterling, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get hotukdeals deal for the full description. A page past the last one returns an empty list.

- Site: hotukdeals.com
- Address: `reduck/hotukdeals.com/list_hot_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hotukdeals.com/list_hot_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hotukdeals.com/list_hot_deals
```

## Input

- `page` (integer, optional): Page of the hot tab, 30 deals a page.

## Output

- `page` (integer, required)
- `deals` (array, required)
- `last_page` (integer | null, optional)

## FAQ

### What does "List hotukdeals hot deals" do?

List the deals on the hot tab of hotukdeals (the UK's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in pounds sterling, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get hotukdeals deal for the full description. A page past the last one returns an empty list.

### How do I automatically list hotukdeals hot deals on hotukdeals.com?

Ask an AI agent connected to Reduck to run reduck/hotukdeals.com/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hotukdeals.com/list_hot_deals

### Is there a hotukdeals.com API to list hotukdeals hot deals?

You do not need one. "List hotukdeals hot deals" drives the real hotukdeals.com pages in a browser, so it works whether or not hotukdeals.com offers an API for this.

### What information do I need to provide?

Optional: page.

### What does it return?

It returns page, deals, last_page.

### Do I need to be logged in to hotukdeals.com?

No. It only uses pages of hotukdeals.com that are reachable without signing in.

### Does it change anything on hotukdeals.com, or only read data?

It only reads. It looks things up on hotukdeals.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hotukdeals.com/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hotukdeals.com/list_hot_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hotukdeals.com/list_hot_deals
