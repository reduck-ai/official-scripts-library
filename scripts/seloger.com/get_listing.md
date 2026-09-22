# Get SeLoger listing

Automatically get SeLoger listing on seloger.com. Fetch a SeLoger property detail page by URL. Returns propertyType, deal, price, pricePerSqm, surface, rooms, bedrooms, floor, location, postalCode, dpe, ges, agency, co-ownership details, and images. Most fields are nullable since not every listing publishes them; energy rating, floor, and co-ownership lots/fees are often missing.

- Site: seloger.com
- Address: `reduck/seloger.com/get_listing`
- Updated: 2026-08-14 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/seloger.com/get_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/seloger.com/get_listing
```

## Input

- `url` (string, required): Detail URL, as returned by seloger search_listings

## Output

- `id` (string | null, required)
- `dpe` (string | null, required)
- `ges` (string | null, required)
- `url` (string, required)
- `deal` (string | null, required)
- `floor` (number | null, required)
- `price` (number | null, required)
- `rooms` (number | null, required)
- `agency` (string | null, required)
- `images` (array, required)
- `surface` (number | null, required)
- `bedrooms` (number | null, required)
- `features` (string | null, required)
- `location` (string | null, required)
- `energyText` (string | null, required)
- `floorTotal` (number | null, required)
- `notaryFees` (number | null, required)
- `postalCode` (string | null, required)
- `description` (string | null, required)
- `pricePerSqm` (number | null, required)
- `propertyType` (string | null, required)
- `coOwnershipFees` (number | null, required)
- `coOwnershipLots` (number | null, required)
- `coOwnershipText` (string | null, required)
- `totalProjectCost` (number | null, required)

## FAQ

### What does "Get SeLoger listing" do?

Fetch a SeLoger property detail page by URL. Returns propertyType, deal, price, pricePerSqm, surface, rooms, bedrooms, floor, location, postalCode, dpe, ges, agency, co-ownership details, and images. Most fields are nullable since not every listing publishes them; energy rating, floor, and co-ownership lots/fees are often missing.

### How do I automatically get SeLoger listing on seloger.com?

Ask an AI agent connected to Reduck to run reduck/seloger.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/seloger.com/get_listing

### Is there a seloger.com API to get SeLoger listing?

You do not need one. "Get SeLoger listing" drives the real seloger.com pages in a browser, so it works whether or not seloger.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, dpe, ges, url, deal, floor, price, rooms, agency, images, surface, bedrooms, features, location, energyText, floorTotal, notaryFees, postalCode, description, pricePerSqm, propertyType, coOwnershipFees, coOwnershipLots, coOwnershipText, totalProjectCost.

### Do I need to be logged in to seloger.com?

No. It only uses pages of seloger.com that are reachable without signing in.

### Does it change anything on seloger.com, or only read data?

It only reads. It looks things up on seloger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/seloger.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/seloger.com/get_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/seloger.com/get_listing
