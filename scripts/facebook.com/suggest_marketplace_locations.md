# Suggest Facebook Marketplace locations

Automatically suggest Facebook Marketplace locations on facebook.com. Look up the places Facebook Marketplace offers for a typed city, neighbourhood or postal code, with the location id that search_marketplace_listings takes. Returns each suggestion's name, subtitle, city, postal code and coordinates. An empty list means Facebook proposed nothing. Changes nothing on the account: the location picker is closed without applying.

- Site: facebook.com
- Address: `reduck/facebook.com/suggest_marketplace_locations`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/suggest_marketplace_locations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/suggest_marketplace_locations
```

## Input

- `query` (string, required): City, neighbourhood or postal code, e.g. Paris or 75014.

## Output

- `locations` (array, required)

## FAQ

### What does "Suggest Facebook Marketplace locations" do?

Look up the places Facebook Marketplace offers for a typed city, neighbourhood or postal code, with the location id that search_marketplace_listings takes. Returns each suggestion's name, subtitle, city, postal code and coordinates. An empty list means Facebook proposed nothing. Changes nothing on the account: the location picker is closed without applying.

### How do I automatically suggest Facebook Marketplace locations on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/suggest_marketplace_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/suggest_marketplace_locations

### Is there a facebook.com API to suggest Facebook Marketplace locations?

You do not need one. "Suggest Facebook Marketplace locations" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns locations.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/suggest_marketplace_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/suggest_marketplace_locations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/suggest_marketplace_locations
