# Doctolib location autocomplete

Resolve free-text location input (city, neighborhood, street) to Doctolib's own place suggestions. Use this before search_practitioners when a plain city name silently resolves to the wrong place (e.g. "Nantes" free text can server-side-match an unrelated city) — pick a suggestion's city/label and pass that into search_practitioners.location instead of raw user input. Does not return the internal URL slug (Doctolib assigns some slugs a disambiguating numeric suffix that isn't derivable from the label alone) — only the city name/label as Doctolib itself would display it.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/autocomplete`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/autocomplete`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/autocomplete
```

## Input

- `query` (string, required): Free-text place query, e.g. 'Nantes', 'Saint-Etienne', 'dentiste' won't work here — this is location-only, not specialty.

## Output

- `results` (array, required)

## FAQ

### What does "Doctolib location autocomplete" do?

Resolve free-text location input (city, neighborhood, street) to Doctolib's own place suggestions. Use this before search_practitioners when a plain city name silently resolves to the wrong place (e.g. "Nantes" free text can server-side-match an unrelated city) — pick a suggestion's city/label and pass that into search_practitioners.location instead of raw user input. Does not return the internal URL slug (Doctolib assigns some slugs a disambiguating numeric suffix that isn't derivable from the label alone) — only the city name/label as Doctolib itself would display it.

### What information do I need to provide?

Required: query.

### What does it return?

It returns results.

### Do I need to be logged in to doctolib.fr?

No. It only uses pages of doctolib.fr that are reachable without signing in.

### Does it change anything on doctolib.fr, or only read data?

It only reads. It looks things up on doctolib.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/autocomplete, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/autocomplete

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/doctolib.fr/autocomplete
