# Bing: set country/region

Automatically set country/region on bing.com. Set Bing's country/region, the setting that decides which country's results Bing searches. It lasts in the browser it runs on, so run it on your own browser before searching; on a fresh browser it has no lasting effect. Pass "auto" to go back to following the browser's location. Returns the country and market Bing reports afterwards.

- Site: bing.com
- Address: `reduck/bing.com/set_country`
- Updated: 2026-09-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bing.com/set_country`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bing.com/set_country
```

## Input

- `country` (string, required): Two-letter country code from Bing's list, e.g. "us", "fr", "de"; or "auto" to follow the browser's location (Bing's "Current country/region").

## Output

- `market` (string | null, required): Bing's market, e.g. "en-US". Language and country are separate settings on Bing, so this can differ from `country`.
- `country` (string, required): The country Bing reports it now searches for, e.g. "US".
- `setting` (string | null, required): Bing's own sentence on its settings page, e.g. "Your country/region is set to United States".

## FAQ

### What does "Bing: set country/region" do?

Set Bing's country/region, the setting that decides which country's results Bing searches. It lasts in the browser it runs on, so run it on your own browser before searching; on a fresh browser it has no lasting effect. Pass "auto" to go back to following the browser's location. Returns the country and market Bing reports afterwards.

### How do I automatically set country/region on bing.com?

Ask an AI agent connected to Reduck to run reduck/bing.com/set_country, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bing.com/set_country

### Is there a bing.com API to set country/region?

You do not need one. "Bing: set country/region" drives the real bing.com pages in a browser, so it works whether or not bing.com offers an API for this.

### What information do I need to provide?

Required: country.

### What does it return?

It returns market, country, setting.

### Do I need to be logged in to bing.com?

No. It only uses pages of bing.com that are reachable without signing in.

### Does it change anything on bing.com, or only read data?

It makes changes on bing.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bing.com/set_country, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bing.com/set_country

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bing.com/set_country
