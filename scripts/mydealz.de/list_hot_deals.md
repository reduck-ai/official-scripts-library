# List mydealz hot deals

Automatically list mydealz hot deals on mydealz.de. List the deals on the hot tab of mydealz (Germany's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in euros, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get mydealz deal for the full description. A page past the last one returns an empty list.

- Site: mydealz.de
- Address: `reduck/mydealz.de/list_hot_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mydealz.de/list_hot_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mydealz.de/list_hot_deals
```

## Input

- `page` (integer, optional): Page of the hot tab, 30 deals a page.

## Output

- `page` (integer, required)
- `deals` (array, required)
- `last_page` (integer | null, optional)

## FAQ

### What does "List mydealz hot deals" do?

List the deals on the hot tab of mydealz (Germany's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in euros, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get mydealz deal for the full description. A page past the last one returns an empty list.

### How do I automatically list mydealz hot deals on mydealz.de?

Ask an AI agent connected to Reduck to run reduck/mydealz.de/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mydealz.de/list_hot_deals

### Is there a mydealz.de API to list mydealz hot deals?

You do not need one. "List mydealz hot deals" drives the real mydealz.de pages in a browser, so it works whether or not mydealz.de offers an API for this.

### What information do I need to provide?

Optional: page.

### What does it return?

It returns page, deals, last_page.

### Do I need to be logged in to mydealz.de?

No. It only uses pages of mydealz.de that are reachable without signing in.

### Does it change anything on mydealz.de, or only read data?

It only reads. It looks things up on mydealz.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mydealz.de/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mydealz.de/list_hot_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mydealz.de/list_hot_deals
