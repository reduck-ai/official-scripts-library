# Suggest Cadremploi locations

Automatically suggest Cadremploi locations on cadremploi.fr. Find the French cities, departments and regions Cadremploi suggests for a place name, with the id each one takes in Cadremploi job searches: a city slug, a department code or a region code. Pass one of them to cadremploi.fr/search_jobs. A name the site does not know returns empty lists.

- Site: cadremploi.fr
- Address: `reduck/cadremploi.fr/suggest_locations`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cadremploi.fr/suggest_locations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cadremploi.fr/suggest_locations
```

## Input

- `query` (string, required): Place name as a person would type it in Cadremploi's location box, e.g. "Lyon", "Gironde" or "Bretagne".

## Output

- `cities` (array, required)
- `regions` (array, required)
- `departments` (array, required)

## FAQ

### What does "Suggest Cadremploi locations" do?

Find the French cities, departments and regions Cadremploi suggests for a place name, with the id each one takes in Cadremploi job searches: a city slug, a department code or a region code. Pass one of them to cadremploi.fr/search_jobs. A name the site does not know returns empty lists.

### How do I automatically suggest Cadremploi locations on cadremploi.fr?

Ask an AI agent connected to Reduck to run reduck/cadremploi.fr/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cadremploi.fr/suggest_locations

### Is there a cadremploi.fr API to suggest Cadremploi locations?

You do not need one. "Suggest Cadremploi locations" drives the real cadremploi.fr pages in a browser, so it works whether or not cadremploi.fr offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns cities, regions, departments.

### Do I need to be logged in to cadremploi.fr?

No. It only uses pages of cadremploi.fr that are reachable without signing in.

### Does it change anything on cadremploi.fr, or only read data?

It only reads. It looks things up on cadremploi.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cadremploi.fr/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cadremploi.fr/suggest_locations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cadremploi.fr/suggest_locations
