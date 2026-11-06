# List my Leboncoin ads

Automatically list my Leboncoin ads on leboncoin.fr. List the online ads of the signed-in Leboncoin account from its "my ads" page: link, ad id and the lines each card shows (title, price, category and creation date). An account with no online ad returns an empty list. Read only; use get_ad_details with a returned link for the full ad.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/list_my_ads`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/list_my_ads`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/list_my_ads
```

## Input

It takes no input.

## Output

- `ads` (array, required)

## FAQ

### What does "List my Leboncoin ads" do?

List the online ads of the signed-in Leboncoin account from its "my ads" page: link, ad id and the lines each card shows (title, price, category and creation date). An account with no online ad returns an empty list. Read only; use get_ad_details with a returned link for the full ad.

### How do I automatically list my Leboncoin ads on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/list_my_ads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/list_my_ads

### Is there a leboncoin.fr API to list my Leboncoin ads?

You do not need one. "List my Leboncoin ads" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns ads.

### Do I need to be logged in to leboncoin.fr?

Yes. It acts as you on leboncoin.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the leboncoin.fr cookies saved by the Reduck extension.

### Does it change anything on leboncoin.fr, or only read data?

It only reads. It looks things up on leboncoin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/list_my_ads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/list_my_ads

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/list_my_ads
