# Suggest Kiwi places

Automatically suggest Kiwi places on kiwi.com. Look up places on Kiwi.com by name, as its From field suggests them: cities, airports, countries and regions, in Kiwi's own relevance order (the first entries are what Kiwi itself suggests first). Returns each place's slug, which kiwi.com/search_flights takes as origin and destination, with its name, type, airport or city code, country and Kiwi's popularity rank. Search by place name; an airport code alone does not always bring up that airport.

- Site: kiwi.com
- Address: `reduck/kiwi.com/suggest_places`
- Updated: 2026-10-12 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kiwi.com/suggest_places`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kiwi.com/suggest_places
```

## Input

- `query` (string, required): A place name as you would type it in Kiwi's From field, e.g. 'Miyazaki', 'Paris', 'Charles de Gaulle'.

## FAQ

### What does "Suggest Kiwi places" do?

Look up places on Kiwi.com by name, as its From field suggests them: cities, airports, countries and regions, in Kiwi's own relevance order (the first entries are what Kiwi itself suggests first). Returns each place's slug, which kiwi.com/search_flights takes as origin and destination, with its name, type, airport or city code, country and Kiwi's popularity rank. Search by place name; an airport code alone does not always bring up that airport.

### How do I automatically suggest Kiwi places on kiwi.com?

Ask an AI agent connected to Reduck to run reduck/kiwi.com/suggest_places, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kiwi.com/suggest_places

### Is there a kiwi.com API to suggest Kiwi places?

You do not need one. "Suggest Kiwi places" drives the real kiwi.com pages in a browser, so it works whether or not kiwi.com offers an API for this.

### What information do I need to provide?

Required: query.

### Do I need to be logged in to kiwi.com?

No. It only uses pages of kiwi.com that are reachable without signing in.

### Does it change anything on kiwi.com, or only read data?

It only reads. It looks things up on kiwi.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kiwi.com/suggest_places, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kiwi.com/suggest_places

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/kiwi.com/suggest_places
