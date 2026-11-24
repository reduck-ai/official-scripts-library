# Suggest Free-Work job locations

Automatically suggest Free-Work job locations on free-work.com. Look up places on Free-Work by name, as its job search's place box suggests them: each with its location key (pass it to free-work.com/search_jobs) and its label. A name Free-Work does not know returns an empty list. Names in several countries come back as several places (Lyon in France and in the United States).

- Site: free-work.com
- Address: `reduck/free-work.com/suggest_locations`
- Updated: 2026-11-23 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/free-work.com/suggest_locations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/free-work.com/suggest_locations
```

## Input

- `query` (string, required): Place name as a person types it, e.g. "Lyon", "Ile-de-France", "Bordeaux".

## Output

- `query` (string, required)
- `locations` (array, required)

## FAQ

### What does "Suggest Free-Work job locations" do?

Look up places on Free-Work by name, as its job search's place box suggests them: each with its location key (pass it to free-work.com/search_jobs) and its label. A name Free-Work does not know returns an empty list. Names in several countries come back as several places (Lyon in France and in the United States).

### How do I automatically suggest Free-Work job locations on free-work.com?

Ask an AI agent connected to Reduck to run reduck/free-work.com/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/free-work.com/suggest_locations

### Is there a free-work.com API to suggest Free-Work job locations?

You do not need one. "Suggest Free-Work job locations" drives the real free-work.com pages in a browser, so it works whether or not free-work.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns query, locations.

### Do I need to be logged in to free-work.com?

No. It only uses pages of free-work.com that are reachable without signing in.

### Does it change anything on free-work.com, or only read data?

It only reads. It looks things up on free-work.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/free-work.com/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/free-work.com/suggest_locations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/free-work.com/suggest_locations
