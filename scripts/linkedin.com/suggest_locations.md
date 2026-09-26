# Suggest LinkedIn locations

Automatically suggest LinkedIn locations on linkedin.com. Resolve a free-text location to LinkedIn geo suggestions [{label, geoUrn}], in ranked order ([0] = best match). The geo equivalent of get_company_info: pass a returned geoUrn to search_people's geoUrn. Returns [] when LinkedIn has no geo for the query (e.g. a continent like 'Europe').

- Site: linkedin.com
- Address: `reduck/linkedin.com/suggest_locations`
- Updated: 2026-09-25 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/suggest_locations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/suggest_locations
```

## Input

- `query` (string, required): Free-text location to look up, e.g. 'Paris', 'London', 'Germany'.
- `limit` (integer, optional): Max suggestions to return.

## Output

- `query` (string, required)
- `locations` (array, required): LinkedIn geo suggestions in ranked order ([0] = best match). Empty when LinkedIn has no geo for the query.

## FAQ

### What does "Suggest LinkedIn locations" do?

Resolve a free-text location to LinkedIn geo suggestions [{label, geoUrn}], in ranked order ([0] = best match). The geo equivalent of get_company_info: pass a returned geoUrn to search_people's geoUrn. Returns [] when LinkedIn has no geo for the query (e.g. a continent like 'Europe').

### How do I automatically suggest LinkedIn locations on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/suggest_locations

### Is there a linkedin.com API to suggest LinkedIn locations?

You do not need one. "Suggest LinkedIn locations" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit.

### What does it return?

It returns query, locations.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/suggest_locations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/suggest_locations
