# Get Zillow listing

Automatically get Zillow listing on zillow.com. Fetch one Zillow property's full detail by zpid (from `search`): address, price, status/type, beds/baths/area, lot, year built, zestimates, geo, description, agent/broker, plus structured rental facts (leaseTerm, furnished, allowedPets, appliances, availabilityDate) — null on for-sale listings.

- Site: zillow.com
- Address: `reduck/zillow.com/get_listing`
- Updated: 2026-09-10 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zillow.com/get_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zillow.com/get_listing
```

## Input

- `zpid` (string, required): Zillow property id, as returned by the search script. The slug-less /homedetails/<zpid>_zpid/ URL redirects to the canonical page, so no address or slug is needed.

## FAQ

### What does "Get Zillow listing" do?

Fetch one Zillow property's full detail by zpid (from `search`): address, price, status/type, beds/baths/area, lot, year built, zestimates, geo, description, agent/broker, plus structured rental facts (leaseTerm, furnished, allowedPets, appliances, availabilityDate) — null on for-sale listings.

### How do I automatically get Zillow listing on zillow.com?

Ask an AI agent connected to Reduck to run reduck/zillow.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/get_listing

### Is there a zillow.com API to get Zillow listing?

You do not need one. "Get Zillow listing" drives the real zillow.com pages in a browser, so it works whether or not zillow.com offers an API for this.

### What information do I need to provide?

Required: zpid.

### Do I need to be logged in to zillow.com?

No. It only uses pages of zillow.com that are reachable without signing in.

### Does it change anything on zillow.com, or only read data?

It only reads. It looks things up on zillow.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zillow.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/get_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/zillow.com/get_listing
