# Vinted — remove an item from favourites

Automatically remove an item from favourites on vinted.com. Remove a Vinted listing from the signed-in account's favourites. Does nothing if it is not currently favourited, and confirms the result by reading the listing's own favourite state back after the change.

- Site: vinted.com
- Address: `reduck/vinted.com/unfavourite_item`
- Updated: 2026-08-14 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vinted.com/unfavourite_item`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vinted.com/unfavourite_item
```

## Input

- `item` (string, required): The listing's full URL, or just its numeric id (e.g. "9660541909" or "https://www.vinted.com/items/9660541909-levis-501").

## Output

- `id` (string, required)
- `url` (string, required)
- `favourited` (boolean, required): The listing's favourite state read back from the page after the run; false once removed.
- `title` (string | null, optional)
- `account_used` (string | null, optional): The signed-in account that performed the action, read from the page.
- `favourites_after` (integer | null, optional)
- `favourites_before` (integer | null, optional): The listing's total favourite count before the change.
- `already_unfavourited` (boolean, optional): True when it was not a favourite and nothing was changed.

## FAQ

### What does "Vinted — remove an item from favourites" do?

Remove a Vinted listing from the signed-in account's favourites. Does nothing if it is not currently favourited, and confirms the result by reading the listing's own favourite state back after the change.

### How do I automatically remove an item from favourites on vinted.com?

Ask an AI agent connected to Reduck to run reduck/vinted.com/unfavourite_item, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/unfavourite_item

### Is there a vinted.com API to remove an item from favourites?

You do not need one. "Vinted — remove an item from favourites" drives the real vinted.com pages in a browser, so it works whether or not vinted.com offers an API for this.

### What information do I need to provide?

Required: item.

### What does it return?

It returns id, url, title, favourited, account_used, favourites_after, favourites_before, already_unfavourited.

### Do I need to be logged in to vinted.com?

Yes. It acts as you on vinted.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vinted.com cookies saved by the Reduck extension.

### Does it change anything on vinted.com, or only read data?

It makes changes on vinted.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vinted.com/unfavourite_item, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/unfavourite_item

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vinted.com/unfavourite_item
