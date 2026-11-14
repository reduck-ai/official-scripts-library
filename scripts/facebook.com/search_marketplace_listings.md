# Search Facebook Marketplace listings

Automatically search Facebook Marketplace listings on facebook.com. Search Facebook Marketplace listings by keyword, with the site's filters: place, price range, sort order, condition, listing age, delivery method, availability and category. Returns each listing's id, link, title, price, city, photo, seller, listing date and status. Without locationId the search uses the account's current Marketplace place and radius; get ids from suggest_marketplace_locations and category ids from list_marketplace_categories. Results load by scroll: count caps how many are returned and complete is true only when Facebook had no more to give. An empty list means nothing matched.

- Site: facebook.com
- Address: `reduck/facebook.com/search_marketplace_listings`
- Updated: 2026-11-13 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/search_marketplace_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/search_marketplace_listings
```

## Input

- `query` (string, required): Keywords to search for.
- `count` (integer, optional)
- `exact` (boolean, optional): Match the keywords exactly.
- `sortBy` (string, optional)
- `maxPrice` (integer, optional)
- `minPrice` (integer, optional)
- `categoryId` (string, optional): Category id from list_marketplace_categories.
- `locationId` (string, optional): Place id from suggest_marketplace_locations. Omit for the account's current Marketplace place. The search radius is the one saved on the account; it cannot be set here.
- `availability` (string, optional): Facebook shows available listings by default.
- `itemCondition` (string, optional)
- `deliveryMethod` (string, optional)
- `daysSinceListed` (integer, optional): Only listings posted in the last 1, 7 or 30 days.

## Output

- `complete` (boolean, required)
- `listings` (array, required)
- `searchUrl` (string, required)

## FAQ

### What does "Search Facebook Marketplace listings" do?

Search Facebook Marketplace listings by keyword, with the site's filters: place, price range, sort order, condition, listing age, delivery method, availability and category. Returns each listing's id, link, title, price, city, photo, seller, listing date and status. Without locationId the search uses the account's current Marketplace place and radius; get ids from suggest_marketplace_locations and category ids from list_marketplace_categories. Results load by scroll: count caps how many are returned and complete is true only when Facebook had no more to give. An empty list means nothing matched.

### How do I automatically search Facebook Marketplace listings on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/search_marketplace_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/search_marketplace_listings

### Is there a facebook.com API to search Facebook Marketplace listings?

You do not need one. "Search Facebook Marketplace listings" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count, exact, sortBy, maxPrice, minPrice, categoryId, locationId, availability, itemCondition, deliveryMethod, daysSinceListed.

### What does it return?

It returns complete, listings, searchUrl.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/search_marketplace_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/search_marketplace_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/search_marketplace_listings
