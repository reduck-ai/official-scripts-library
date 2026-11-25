# List Dealabs hot deals

Automatically list Dealabs hot deals on dealabs.com. List the deals on the hot tab of Dealabs (France's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in euros, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get Dealabs deal for the full description. A page past the last one returns an empty list.

- Site: dealabs.com
- Address: `reduck/dealabs.com/list_hot_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dealabs.com/list_hot_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dealabs.com/list_hot_deals
```

## Input

- `page` (integer, optional): Page of the hot tab, 30 deals a page.

## Output

- `page` (integer, required)
- `deals` (array, required)
- `last_page` (integer | null, optional)

## FAQ

### What does "List Dealabs hot deals" do?

List the deals on the hot tab of Dealabs (France's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in euros, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get Dealabs deal for the full description. A page past the last one returns an empty list.

### How do I automatically list Dealabs hot deals on dealabs.com?

Ask an AI agent connected to Reduck to run reduck/dealabs.com/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dealabs.com/list_hot_deals

### Is there a dealabs.com API to list Dealabs hot deals?

You do not need one. "List Dealabs hot deals" drives the real dealabs.com pages in a browser, so it works whether or not dealabs.com offers an API for this.

### What information do I need to provide?

Optional: page.

### What does it return?

It returns page, deals, last_page.

### Do I need to be logged in to dealabs.com?

No. It only uses pages of dealabs.com that are reachable without signing in.

### Does it change anything on dealabs.com, or only read data?

It only reads. It looks things up on dealabs.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dealabs.com/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dealabs.com/list_hot_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dealabs.com/list_hot_deals
