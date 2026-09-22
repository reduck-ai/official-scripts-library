# Search companies

Automatically search companies on glassdoor.com. Search Glassdoor employers by name → list of {employerId, name, shortName, logo, website}. Returns ~10 fuzzy matches ranked by Glassdoor's own employer search suggestions — near-name and substring matches are included (e.g. "Airbus" also yields "Air Busan"), and an exact match is not guaranteed to be first. logo/website/shortName may be null. The employerId feeds get_company and the other employer-scoped scripts. Anonymous, read-only.

- Site: glassdoor.com
- Address: `reduck/glassdoor.com/search_companies`
- Updated: 2026-08-24 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/glassdoor.com/search_companies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/search_companies
```

## Input

- `query` (string, required): Company name to search, e.g. "Google" or "Goldman Sachs".

## FAQ

### What does "Search companies" do?

Search Glassdoor employers by name → list of {employerId, name, shortName, logo, website}. Returns ~10 fuzzy matches ranked by Glassdoor's own employer search suggestions — near-name and substring matches are included (e.g. "Airbus" also yields "Air Busan"), and an exact match is not guaranteed to be first. logo/website/shortName may be null. The employerId feeds get_company and the other employer-scoped scripts. Anonymous, read-only.

### How do I automatically search companies on glassdoor.com?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/search_companies

### Is there a glassdoor.com API to search companies?

You do not need one. "Search companies" drives the real glassdoor.com pages in a browser, so it works whether or not glassdoor.com offers an API for this.

### What information do I need to provide?

Required: query.

### Do I need to be logged in to glassdoor.com?

No. It only uses pages of glassdoor.com that are reachable without signing in.

### Does it change anything on glassdoor.com, or only read data?

It only reads. It looks things up on glassdoor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/search_companies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/glassdoor.com/search_companies
