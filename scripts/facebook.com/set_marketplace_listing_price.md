# Set the price of a Facebook Marketplace listing

Automatically set the price of a Facebook Marketplace listing on facebook.com. Change the price of one of your own Facebook Marketplace listings, by its listing id from list_my_marketplace_listings. Only the price changes: the title and the other fields are left as they are, and the script refuses to save if the title moved. Facebook shows the old price struck through next to the new one. Returns the title, the price before and the price after as read back from the listing.

- Site: facebook.com
- Address: `reduck/facebook.com/set_marketplace_listing_price`
- Updated: 2026-11-16 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/set_marketplace_listing_price`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/set_marketplace_listing_price
```

## Input

- `price` (integer, required): New price in the account's currency, whole units.
- `listingId` (string, required): Listing id from list_my_marketplace_listings.

## Output

- `title` (string, required)
- `listingId` (string, required)
- `priceAfter` (string, required)
- `priceBefore` (string, required)

## FAQ

### What does "Set the price of a Facebook Marketplace listing" do?

Change the price of one of your own Facebook Marketplace listings, by its listing id from list_my_marketplace_listings. Only the price changes: the title and the other fields are left as they are, and the script refuses to save if the title moved. Facebook shows the old price struck through next to the new one. Returns the title, the price before and the price after as read back from the listing.

### How do I automatically set the price of a Facebook Marketplace listing on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/set_marketplace_listing_price, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/set_marketplace_listing_price

### Is there a facebook.com API to set the price of a Facebook Marketplace listing?

You do not need one. "Set the price of a Facebook Marketplace listing" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: listingId, price.

### What does it return?

It returns title, listingId, priceAfter, priceBefore.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/set_marketplace_listing_price, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/set_marketplace_listing_price

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/set_marketplace_listing_price
