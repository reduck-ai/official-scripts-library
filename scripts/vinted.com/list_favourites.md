# Vinted — list favourited items

Automatically list favourited items on vinted.com. List the items the signed-in Vinted account has favourited, with each one's title, brand, size, condition, price, total price with Buyer Protection, photo and link.

- Site: vinted.com
- Address: `reduck/vinted.com/list_favourites`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vinted.com/list_favourites`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vinted.com/list_favourites
```

## Input

It takes no input.

## Output

- `items` (array, required)

## FAQ

### What does "Vinted — list favourited items" do?

List the items the signed-in Vinted account has favourited, with each one's title, brand, size, condition, price, total price with Buyer Protection, photo and link.

### How do I automatically list favourited items on vinted.com?

Ask an AI agent connected to Reduck to run reduck/vinted.com/list_favourites, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/list_favourites

### Is there a vinted.com API to list favourited items?

You do not need one. "Vinted — list favourited items" drives the real vinted.com pages in a browser, so it works whether or not vinted.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items.

### Do I need to be logged in to vinted.com?

Yes. It acts as you on vinted.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vinted.com cookies saved by the Reduck extension.

### Does it change anything on vinted.com, or only read data?

It only reads. It looks things up on vinted.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vinted.com/list_favourites, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/list_favourites

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vinted.com/list_favourites
