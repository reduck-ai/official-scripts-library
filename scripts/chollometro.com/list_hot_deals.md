# List Chollometro hot deals

Automatically list Chollometro hot deals on chollometro.com. List the deals on the rising (hot) tab of Chollometro (Spain's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in euros, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get Chollometro deal for the full description. A page past the last one returns an empty list.

- Site: chollometro.com
- Address: `reduck/chollometro.com/list_hot_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chollometro.com/list_hot_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chollometro.com/list_hot_deals
```

## Input

- `page` (integer, optional): Page of the hot tab, 30 deals a page.

## Output

- `page` (integer, required)
- `deals` (array, required)
- `last_page` (integer | null, optional)

## FAQ

### What does "List Chollometro hot deals" do?

List the deals on the rising (hot) tab of Chollometro (Spain's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in euros, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get Chollometro deal for the full description. A page past the last one returns an empty list.

### How do I automatically list Chollometro hot deals on chollometro.com?

Ask an AI agent connected to Reduck to run reduck/chollometro.com/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chollometro.com/list_hot_deals

### Is there a chollometro.com API to list Chollometro hot deals?

You do not need one. "List Chollometro hot deals" drives the real chollometro.com pages in a browser, so it works whether or not chollometro.com offers an API for this.

### What information do I need to provide?

Optional: page.

### What does it return?

It returns page, deals, last_page.

### Do I need to be logged in to chollometro.com?

No. It only uses pages of chollometro.com that are reachable without signing in.

### Does it change anything on chollometro.com, or only read data?

It only reads. It looks things up on chollometro.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chollometro.com/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chollometro.com/list_hot_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/chollometro.com/list_hot_deals
