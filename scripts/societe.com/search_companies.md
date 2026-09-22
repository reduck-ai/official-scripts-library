# Search companies

Automatically search companies on societe.com. Search societe.com for French companies by name or keyword. Returns query, url, count, and companies (each with siren, name, url, activity, address).

- Site: societe.com
- Address: `reduck/societe.com/search_companies`
- Updated: 2026-09-11 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/societe.com/search_companies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/societe.com/search_companies
```

## Input

- `query` (string, required)
- `limit` (integer, optional)

## Output

- `url` (string, required)
- `count` (number, required)
- `query` (string, required)
- `companies` (array, required)

## FAQ

### What does "Search companies" do?

Search societe.com for French companies by name or keyword. Returns query, url, count, and companies (each with siren, name, url, activity, address).

### How do I automatically search companies on societe.com?

Ask an AI agent connected to Reduck to run reduck/societe.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/societe.com/search_companies

### Is there a societe.com API to search companies?

You do not need one. "Search companies" drives the real societe.com pages in a browser, so it works whether or not societe.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit.

### What does it return?

It returns url, count, query, companies.

### Do I need to be logged in to societe.com?

No. It only uses pages of societe.com that are reachable without signing in.

### Does it change anything on societe.com, or only read data?

It only reads. It looks things up on societe.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/societe.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/societe.com/search_companies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/societe.com/search_companies
