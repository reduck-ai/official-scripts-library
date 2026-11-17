# Get Facebook Marketplace seller profile

Automatically get Facebook Marketplace seller profile on facebook.com. Read a seller's Facebook Marketplace profile by user id or profile link: name, join date, number of active listings, follower count, rating figures when public, and their active listings with id, title, price and place. Get the seller id from search_marketplace_listings or get_marketplace_listing. Ratings are null when the seller keeps them private. Does not follow or message the seller.

- Site: facebook.com
- Address: `reduck/facebook.com/get_marketplace_seller`
- Updated: 2026-11-16 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/get_marketplace_seller`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_marketplace_seller
```

## Input

- `seller` (string, required): Seller's Facebook user id, or a Marketplace profile link.

## Output

- `id` (string, required)
- `listings` (array, required)
- `name` (string | null, optional)
- `joinedAt` (string | null, optional): ISO time Facebook records for the registration.
- `followers` (integer | null, optional)
- `ratingCount` (integer | null, optional)
- `ratingAverage` (number | null, optional)
- `ratingsArePrivate` (boolean | null, optional)
- `activeListingsCount` (integer | null, optional)

## FAQ

### What does "Get Facebook Marketplace seller profile" do?

Read a seller's Facebook Marketplace profile by user id or profile link: name, join date, number of active listings, follower count, rating figures when public, and their active listings with id, title, price and place. Get the seller id from search_marketplace_listings or get_marketplace_listing. Ratings are null when the seller keeps them private. Does not follow or message the seller.

### How do I automatically get Facebook Marketplace seller profile on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_marketplace_seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_marketplace_seller

### Is there a facebook.com API to get Facebook Marketplace seller profile?

You do not need one. "Get Facebook Marketplace seller profile" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: seller.

### What does it return?

It returns id, name, joinedAt, listings, followers, ratingCount, ratingAverage, ratingsArePrivate, activeListingsCount.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_marketplace_seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_marketplace_seller

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/get_marketplace_seller
