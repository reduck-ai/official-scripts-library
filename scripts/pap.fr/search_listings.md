# Search PAP.fr property listings

Automatically search PAP.fr property listings on pap.fr. Search PAP.fr, the French classifieds site where owners list property directly without an agency, and return the listings on the results page: the listing's id and link, asking price in euros, town and postcode, number of rooms and bedrooms, floor area, and the owner's description.

- Site: pap.fr
- Address: `reduck/pap.fr/search_listings`
- Updated: 2026-09-18 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pap.fr/search_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pap.fr/search_listings
```

## Input

- `location` (string, required): Where to search, as typed into the site's search box: a town ("Bordeaux"), postcode, department or region. The first suggestion the site offers is taken, and the label it resolved to is returned as resolvedLocation.
- `count` (integer, optional): How many listings to collect. A results page holds about 15, so a larger count walks on through further pages and stops early when the results run out.
- `max_price` (integer, optional): Maximum price in euros (the purchase price, or the monthly rent for a rental).
- `transaction` (string, optional): vente = for sale, location = long-term rental, vacances = holiday rental.
- `property_type` (string, optional): Restrict to one property type. Omitted means every type the site returns for that search.

## Output

- `listings` (array, required)
- `returned` (integer, required)
- `searchUrl` (string, required): The results page the search landed on.
- `transaction` (string, required)
- `noExactMatches` (boolean, required): True when the search matched nothing and the site offered listings from a wider search instead. listings is then empty.
- `resolvedLocation` (string, required): The location label the site matched, e.g. "Bordeaux (33)". Compare it with what was asked for: a town name that exists in several departments can resolve to another one.

## FAQ

### What does "Search PAP.fr property listings" do?

Search PAP.fr, the French classifieds site where owners list property directly without an agency, and return the listings on the results page: the listing's id and link, asking price in euros, town and postcode, number of rooms and bedrooms, floor area, and the owner's description.

### How do I automatically search PAP.fr property listings on pap.fr?

Ask an AI agent connected to Reduck to run reduck/pap.fr/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pap.fr/search_listings

### Is there a pap.fr API to search PAP.fr property listings?

You do not need one. "Search PAP.fr property listings" drives the real pap.fr pages in a browser, so it works whether or not pap.fr offers an API for this.

### What information do I need to provide?

Required: location. Optional: count, max_price, transaction, property_type.

### What does it return?

It returns listings, returned, searchUrl, transaction, noExactMatches, resolvedLocation.

### Do I need to be logged in to pap.fr?

No. It only uses pages of pap.fr that are reachable without signing in.

### Does it change anything on pap.fr, or only read data?

It only reads. It looks things up on pap.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pap.fr/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pap.fr/search_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pap.fr/search_listings
