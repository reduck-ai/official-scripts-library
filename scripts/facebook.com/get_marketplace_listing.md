# Get Facebook Marketplace listing

Automatically get Facebook Marketplace listing on facebook.com. Read one Facebook Marketplace listing by its id or link: title, price, description, condition and other attributes, place, all photos, listing date, status (available, pending, sold) and delivery options, plus the seller's name, id and rating figures. A listing that was removed or is not visible to this account returns an error rather than an empty record. Opening it does not message the seller.

- Site: facebook.com
- Address: `reduck/facebook.com/get_marketplace_listing`
- Updated: 2026-11-18 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/get_marketplace_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_marketplace_listing
```

## Input

- `listing` (string, required): Listing id or full Marketplace item link, from search_marketplace_listings.

## Output

- `id` (string, required)
- `url` (string, required)
- `photos` (array, required)
- `seller` (object, required)
- `attributes` (array, required)
- `categoryPath` (array, required)
- `deliveryTypes` (array, required)
- `price` (string | null, optional)
- `title` (string | null, optional)
- `isSold` (boolean | null, optional)
- `status` (string | null, optional): Facebook's listing status, e.g. AVAILABLE.
- `isYours` (boolean | null, optional)
- `currency` (string | null, optional)
- `latitude` (number | null, optional)
- `listedAt` (string | null, optional)
- `location` (string | null, optional)
- `isPending` (boolean | null, optional)
- `longitude` (number | null, optional)
- `canMessage` (boolean | null, optional)
- `description` (string | null, optional)
- `priceAmount` (number | null, optional)
- `shippingOffered` (boolean | null, optional)

## FAQ

### What does "Get Facebook Marketplace listing" do?

Read one Facebook Marketplace listing by its id or link: title, price, description, condition and other attributes, place, all photos, listing date, status (available, pending, sold) and delivery options, plus the seller's name, id and rating figures. A listing that was removed or is not visible to this account returns an error rather than an empty record. Opening it does not message the seller.

### How do I automatically get Facebook Marketplace listing on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_marketplace_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_marketplace_listing

### Is there a facebook.com API to get Facebook Marketplace listing?

You do not need one. "Get Facebook Marketplace listing" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: listing.

### What does it return?

It returns id, url, price, title, isSold, photos, seller, status, isYours, currency, latitude, listedAt, location, isPending, longitude, attributes, canMessage, description, priceAmount, categoryPath, deliveryTypes, shippingOffered.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_marketplace_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_marketplace_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/get_marketplace_listing
