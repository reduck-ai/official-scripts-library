# Remove train ticket from SNCF Connect cart

Automatically remove train ticket from SNCF Connect cart on sncf-connect.com. Remove a specific train ticket from the SNCF Connect cart (or the only one if there's just one). Requires login. Pass `match` (substring of origin/destination, e.g. "Bordeaux") to pick which item when the cart has several; omitted `match` is fine only when exactly one item is in the cart. Confirms the site's own removal dialog. To empty the whole cart, call once per item. Runs only via the local browser extension, not the hosted cloud browser.

- Site: sncf-connect.com
- Address: `reduck/sncf-connect.com/remove_from_cart`
- Updated: 2026-09-08 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sncf-connect.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/remove_from_cart
```

## Input

- `match` (string, optional): Substring of the item's origin or destination station as displayed on SNCF Connect (e.g. "Lyon Part Dieu", "Torino Porta Susa" — the site uses local-language station names, not English ones like "Turin"). Required if the cart has more than one item.
- `confirm` (boolean, optional): false = dry-run (report + dismiss, cart unchanged); true = actually remove the item

## Output

- `dryRun` (boolean, required)
- `removed` (boolean, required)
- `itemsRemaining` (integer, required)
- `cartEmpty` (boolean, optional)
- `removedItem` (object | null, optional)

## FAQ

### What does "Remove train ticket from SNCF Connect cart" do?

Remove a specific train ticket from the SNCF Connect cart (or the only one if there's just one). Requires login. Pass `match` (substring of origin/destination, e.g. "Bordeaux") to pick which item when the cart has several; omitted `match` is fine only when exactly one item is in the cart. Confirms the site's own removal dialog. To empty the whole cart, call once per item. Runs only via the local browser extension, not the hosted cloud browser.

### How do I automatically remove train ticket from SNCF Connect cart on sncf-connect.com?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/remove_from_cart

### Is there a sncf-connect.com API to remove train ticket from SNCF Connect cart?

You do not need one. "Remove train ticket from SNCF Connect cart" drives the real sncf-connect.com pages in a browser, so it works whether or not sncf-connect.com offers an API for this.

### What information do I need to provide?

Optional: match, confirm.

### What does it return?

It returns dryRun, removed, cartEmpty, removedItem, itemsRemaining.

### Do I need to be logged in to sncf-connect.com?

Yes. It acts as you on sncf-connect.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the sncf-connect.com cookies saved by the Reduck extension.

### Does it change anything on sncf-connect.com, or only read data?

It makes changes on sncf-connect.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/remove_from_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sncf-connect.com/remove_from_cart
