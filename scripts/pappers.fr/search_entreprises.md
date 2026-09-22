# Search Pappers companies

Automatically search Pappers companies on pappers.fr. Search French companies on Pappers by name, or look one up directly by its SIREN or SIRET. Returns each company with its legal form, main activity, head-office address, workforce bracket, share capital, creation date and status. A name search pages through up to 400 results. An identifier lookup returns the single matching company and includes its head-office SIRET, but Pappers does not provide share capital or workforce figures on that route.

- Site: pappers.fr
- Address: `reduck/pappers.fr/search_entreprises`
- Updated: 2026-09-01 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pappers.fr/search_entreprises`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pappers.fr/search_entreprises
```

## Input

- `q` (string, optional): Search text (company name, SIREN, etc.). Must be non-empty: an empty string is treated by Pappers as an unfiltered match-everything query.
- `page` (integer, optional): Results page (20 per page by default). Pappers caps pagination at 400 entities, so page x par_page must be <= 400.
- `query` (string, optional): Alias for q. Supply either q or query, not both; if both are given, q wins.
- `par_page` (integer, optional): Number of results per page (max 100). Pappers caps pagination at 400 entities, so page x par_page must be <= 400.

## Output

- `page` (integer, optional)
- `total` (integer, optional): Total number of companies matching the query
- `par_page` (integer, optional)
- `resultats` (array, optional)

## FAQ

### What does "Search Pappers companies" do?

Search French companies on Pappers by name, or look one up directly by its SIREN or SIRET. Returns each company with its legal form, main activity, head-office address, workforce bracket, share capital, creation date and status. A name search pages through up to 400 results. An identifier lookup returns the single matching company and includes its head-office SIRET, but Pappers does not provide share capital or workforce figures on that route.

### How do I automatically search Pappers companies on pappers.fr?

Ask an AI agent connected to Reduck to run reduck/pappers.fr/search_entreprises, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pappers.fr/search_entreprises

### Is there a pappers.fr API to search Pappers companies?

You do not need one. "Search Pappers companies" drives the real pappers.fr pages in a browser, so it works whether or not pappers.fr offers an API for this.

### What information do I need to provide?

Optional: q, page, query, par_page.

### What does it return?

It returns page, total, par_page, resultats.

### Do I need to be logged in to pappers.fr?

No. It only uses pages of pappers.fr that are reachable without signing in.

### Does it change anything on pappers.fr, or only read data?

It only reads. It looks things up on pappers.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pappers.fr/search_entreprises, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pappers.fr/search_entreprises

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pappers.fr/search_entreprises
