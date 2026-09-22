# Search Barreau de Nantes lawyers

Automatically search Barreau de Nantes lawyers on barreaunantes.fr. Search the Nantes bar association's public lawyer directory by SURNAME (the site's own "Nom" field). Matching is substring and accent-insensitive on the surname only — a given name ("gaetane") or a cabinet name ("FIDAL") returns no rows, verified. Returns each match's slug (the join key for get_lawyer), surname, given name, cabinet and city. No login required. The directory renders its whole result set on one page, so a one-letter query can return hundreds of rows; an empty list means no surname matches.

- Site: barreaunantes.fr
- Address: `reduck/barreaunantes.fr/list_lawyers`
- Updated: 2026-09-21 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/barreaunantes.fr/list_lawyers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/barreaunantes.fr/list_lawyers
```

## Input

- `nom` (string, required): Name (or partial name) to search for, matching the site's own "Nom" search field.

## Output

- `count` (integer, required): Number of matching lawyers returned. The directory renders its whole result set on one page, so this is the complete match count, not a page size (a one-letter query can return several hundred).
- `query` (string, required): The normalised name that was actually submitted to the site's search form.
- `lawyers` (array, required): Matching lawyers. The site substring-matches, so short queries match broadly. An empty array is a legitimate outcome meaning no lawyer matches this name; it is only ever returned after the search form was confirmed submitted.

## FAQ

### What does "Search Barreau de Nantes lawyers" do?

Search the Nantes bar association's public lawyer directory by SURNAME (the site's own "Nom" field). Matching is substring and accent-insensitive on the surname only — a given name ("gaetane") or a cabinet name ("FIDAL") returns no rows, verified. Returns each match's slug (the join key for get_lawyer), surname, given name, cabinet and city. No login required. The directory renders its whole result set on one page, so a one-letter query can return hundreds of rows; an empty list means no surname matches.

### How do I automatically search Barreau de Nantes lawyers on barreaunantes.fr?

Ask an AI agent connected to Reduck to run reduck/barreaunantes.fr/list_lawyers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/barreaunantes.fr/list_lawyers

### Is there a barreaunantes.fr API to search Barreau de Nantes lawyers?

You do not need one. "Search Barreau de Nantes lawyers" drives the real barreaunantes.fr pages in a browser, so it works whether or not barreaunantes.fr offers an API for this.

### What information do I need to provide?

Required: nom.

### What does it return?

It returns count, query, lawyers.

### Do I need to be logged in to barreaunantes.fr?

No. It only uses pages of barreaunantes.fr that are reachable without signing in.

### Does it change anything on barreaunantes.fr, or only read data?

It only reads. It looks things up on barreaunantes.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/barreaunantes.fr/list_lawyers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/barreaunantes.fr/list_lawyers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/barreaunantes.fr/list_lawyers
