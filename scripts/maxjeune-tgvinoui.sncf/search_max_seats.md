# Search remaining MAX JEUNE seats per train on SNCF Max Planner

Automatically search remaining MAX JEUNE seats per train on SNCF Max Planner on maxjeune-tgvinoui.sncf. Searches the SNCF MAX JEUNE / MAX ACTIF Max Planner between two stations and returns, for each of the next 30 days starting today (the site's full booking window), every train with MAX seats still available and how many seats remain. A day the site has no data for yet, or failed to answer, is returned with that reason and no trains. A station name that matches several stations fails and lists them.

- Site: maxjeune-tgvinoui.sncf
- Address: `reduck/maxjeune-tgvinoui.sncf/search_max_seats`
- Updated: 2026-10-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/maxjeune-tgvinoui.sncf/search_max_seats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/maxjeune-tgvinoui.sncf/search_max_seats
```

## Input

- `origin` (string, required): Departure station name (e.g. "Paris Gare de Lyon"). Must match one of the site's station suggestions exactly, unless the name has a single suggestion; otherwise the run fails and lists the candidates.
- `destination` (string, required): Arrival station name (e.g. "Marseille Saint-Charles"). Same matching rule as origin.

## Output

- `days` (array, required)
- `origin` (object, required)
- `destination` (object, required)

## FAQ

### What does "Search remaining MAX JEUNE seats per train on SNCF Max Planner" do?

Searches the SNCF MAX JEUNE / MAX ACTIF Max Planner between two stations and returns, for each of the next 30 days starting today (the site's full booking window), every train with MAX seats still available and how many seats remain. A day the site has no data for yet, or failed to answer, is returned with that reason and no trains. A station name that matches several stations fails and lists them.

### How do I automatically search remaining MAX JEUNE seats per train on SNCF Max Planner on maxjeune-tgvinoui.sncf?

Ask an AI agent connected to Reduck to run reduck/maxjeune-tgvinoui.sncf/search_max_seats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/maxjeune-tgvinoui.sncf/search_max_seats

### Is there a maxjeune-tgvinoui.sncf API to search remaining MAX JEUNE seats per train on SNCF Max Planner?

You do not need one. "Search remaining MAX JEUNE seats per train on SNCF Max Planner" drives the real maxjeune-tgvinoui.sncf pages in a browser, so it works whether or not maxjeune-tgvinoui.sncf offers an API for this.

### What information do I need to provide?

Required: origin, destination.

### What does it return?

It returns days, origin, destination.

### Do I need to be logged in to maxjeune-tgvinoui.sncf?

No. It only uses pages of maxjeune-tgvinoui.sncf that are reachable without signing in.

### Does it change anything on maxjeune-tgvinoui.sncf, or only read data?

It only reads. It looks things up on maxjeune-tgvinoui.sncf and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/maxjeune-tgvinoui.sncf/search_max_seats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/maxjeune-tgvinoui.sncf/search_max_seats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/maxjeune-tgvinoui.sncf/search_max_seats
