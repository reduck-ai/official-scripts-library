# List my Facebook Marketplace listings

Automatically list my Facebook Marketplace listings on facebook.com. List the items the signed-in account is selling on Facebook Marketplace: id, link, title, price, status (available, in review, sold), whether it is sold and when it was created. Scrolls to load the whole list. An account with nothing for sale returns an empty list. Read only.

- Site: facebook.com
- Address: `reduck/facebook.com/list_my_marketplace_listings`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/list_my_marketplace_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_my_marketplace_listings
```

## Input

It takes no input.

## Output

- `listings` (array, required)

## FAQ

### What does "List my Facebook Marketplace listings" do?

List the items the signed-in account is selling on Facebook Marketplace: id, link, title, price, status (available, in review, sold), whether it is sold and when it was created. Scrolls to load the whole list. An account with nothing for sale returns an empty list. Read only.

### How do I automatically list my Facebook Marketplace listings on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_my_marketplace_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_my_marketplace_listings

### Is there a facebook.com API to list my Facebook Marketplace listings?

You do not need one. "List my Facebook Marketplace listings" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns listings.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_my_marketplace_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_my_marketplace_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/list_my_marketplace_listings
