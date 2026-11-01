# Suggest Trainline stations and cities

Automatically suggest Trainline stations and cities on thetrainline.com. Look up stations and cities on Trainline by name, as its From and To fields suggest them while you type, in Trainline's own order. Returns each place's name, type (station or city), country code and Trainline code, which thetrainline.com/search_journeys takes as origin and destination. Trainline's matching is loose: a name it does not know can still bring up an unrelated place, so check the names before you search. A text Trainline has no suggestion for returns an empty list.

- Site: thetrainline.com
- Address: `reduck/thetrainline.com/suggest_locations`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/thetrainline.com/suggest_locations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/thetrainline.com/suggest_locations
```

## Input

- `query` (string, required): A station or city name, as you would type it in Trainline's From field, e.g. 'Munich' or 'Paris Gare de Lyon'.

## Output

- `locations` (array, required): Trainline's suggestions, in its order. Empty when it has none.

## FAQ

### What does "Suggest Trainline stations and cities" do?

Look up stations and cities on Trainline by name, as its From and To fields suggest them while you type, in Trainline's own order. Returns each place's name, type (station or city), country code and Trainline code, which thetrainline.com/search_journeys takes as origin and destination. Trainline's matching is loose: a name it does not know can still bring up an unrelated place, so check the names before you search. A text Trainline has no suggestion for returns an empty list.

### How do I automatically suggest Trainline stations and cities on thetrainline.com?

Ask an AI agent connected to Reduck to run reduck/thetrainline.com/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/thetrainline.com/suggest_locations

### Is there a thetrainline.com API to suggest Trainline stations and cities?

You do not need one. "Suggest Trainline stations and cities" drives the real thetrainline.com pages in a browser, so it works whether or not thetrainline.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns locations.

### Do I need to be logged in to thetrainline.com?

No. It only uses pages of thetrainline.com that are reachable without signing in.

### Does it change anything on thetrainline.com, or only read data?

It only reads. It looks things up on thetrainline.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/thetrainline.com/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/thetrainline.com/suggest_locations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/thetrainline.com/suggest_locations
