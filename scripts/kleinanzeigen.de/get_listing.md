# Get Kleinanzeigen listing details

Automatically get Kleinanzeigen listing details on kleinanzeigen.de. Get the full details of a Kleinanzeigen listing from its link or id: title, price, location, posting date, full description, attributes such as condition or type, whether the seller is a private person or a business (businesses are named) with a link to the seller's other listings, and all photos.

- Site: kleinanzeigen.de
- Address: `reduck/kleinanzeigen.de/get_listing`
- Updated: 2026-10-06 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kleinanzeigen.de/get_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kleinanzeigen.de/get_listing
```

## Input

- `listing` (string, required): The listing's Kleinanzeigen link (https://www.kleinanzeigen.de/s-anzeige/...) or its numeric id, as returned by search_listings.

## Output

- `id` (string, required)
- `url` (string, required)
- `title` (string, required)
- `price` (number | null, optional)
- `images` (array, optional)
- `posted` (string | null, optional): Posting date as shown (DD.MM.YYYY).
- `seller` (object | null, optional)
- `features` (array, optional)
- `location` (string | null, optional): Postal code, state and town as shown.
- `priceText` (string | null, optional): Price as shown, e.g. "120 €" or "900 € VB" (VB = negotiable).
- `attributes` (array, optional): Listing attributes as the site labels them (in German), e.g. Zustand (condition), Art, Typ.
- `description` (string | null, optional)

## FAQ

### What does "Get Kleinanzeigen listing details" do?

Get the full details of a Kleinanzeigen listing from its link or id: title, price, location, posting date, full description, attributes such as condition or type, whether the seller is a private person or a business (businesses are named) with a link to the seller's other listings, and all photos.

### How do I automatically get Kleinanzeigen listing details on kleinanzeigen.de?

Ask an AI agent connected to Reduck to run reduck/kleinanzeigen.de/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kleinanzeigen.de/get_listing

### Is there a kleinanzeigen.de API to get Kleinanzeigen listing details?

You do not need one. "Get Kleinanzeigen listing details" drives the real kleinanzeigen.de pages in a browser, so it works whether or not kleinanzeigen.de offers an API for this.

### What information do I need to provide?

Required: listing.

### What does it return?

It returns id, url, price, title, images, posted, seller, features, location, priceText, attributes, description.

### Do I need to be logged in to kleinanzeigen.de?

No. It only uses pages of kleinanzeigen.de that are reachable without signing in.

### Does it change anything on kleinanzeigen.de, or only read data?

It only reads. It looks things up on kleinanzeigen.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kleinanzeigen.de/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kleinanzeigen.de/get_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/kleinanzeigen.de/get_listing
