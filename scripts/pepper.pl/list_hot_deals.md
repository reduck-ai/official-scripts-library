# List Pepper.pl hot deals

Automatically list Pepper.pl hot deals on pepper.pl. List the deals on the hottest tab of Pepper.pl (Poland's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in złoty, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get Pepper.pl deal for the full description. A page past the last one returns an empty list.

- Site: pepper.pl
- Address: `reduck/pepper.pl/list_hot_deals`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pepper.pl/list_hot_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pepper.pl/list_hot_deals
```

## Input

- `page` (integer, optional): Page of the hottest tab, 30 deals a page.

## Output

- `page` (integer, required)
- `deals` (array, required)
- `last_page` (integer | null, optional)

## FAQ

### What does "List Pepper.pl hot deals" do?

List the deals on the hottest tab of Pepper.pl (Poland's deal community), one page of 30 at a time, in the order the site shows them. Each deal has its id, link, title, type (deal or voucher), temperature (the community vote), price and previous price in złoty, discount, shipping, voucher code, merchant, category, image, who posted it, comment count, dates, and whether it is expired or local. Pass the id or link to Get Pepper.pl deal for the full description. A page past the last one returns an empty list.

### How do I automatically list Pepper.pl hot deals on pepper.pl?

Ask an AI agent connected to Reduck to run reduck/pepper.pl/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pepper.pl/list_hot_deals

### Is there a pepper.pl API to list Pepper.pl hot deals?

You do not need one. "List Pepper.pl hot deals" drives the real pepper.pl pages in a browser, so it works whether or not pepper.pl offers an API for this.

### What information do I need to provide?

Optional: page.

### What does it return?

It returns page, deals, last_page.

### Do I need to be logged in to pepper.pl?

No. It only uses pages of pepper.pl that are reachable without signing in.

### Does it change anything on pepper.pl, or only read data?

It only reads. It looks things up on pepper.pl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pepper.pl/list_hot_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pepper.pl/list_hot_deals

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/pepper.pl/list_hot_deals
