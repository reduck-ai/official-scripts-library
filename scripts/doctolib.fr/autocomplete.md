# Doctolib location autocomplete

Doctolib place suggestions for a free-text location (city, neighborhood, street): each with the label and city as Doctolib shows them, the context line, the address for a street, the country and the Google place id. Returns [] when Doctolib suggests nothing.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/autocomplete`
- Updated: 2026-11-06 (v1)
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

Doctolib place suggestions for a free-text location (city, neighborhood, street): each with the label and city as Doctolib shows them, the context line, the address for a street, the country and the Google place id. Returns [] when Doctolib suggests nothing.

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
