# Search Trustpilot companies

Automatically search Trustpilot companies on trustpilot.com. Search Trustpilot businesses by name/keyword. Returns each company's identifyingName (the domain key used by get_company/get_reviews), TrustScore, stars, review count, location, contact and categories. Paginated.

- Site: trustpilot.com
- Address: `reduck/trustpilot.com/search_company`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trustpilot.com/search_company`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/search_company
```

## Input

- `query` (string, required): Company name or keyword, e.g. "nike".
- `page` (integer, optional): 1-based results page (pageSize 10).

## Output

- `query` (string, required)
- `hasMore` (boolean, required)
- `businesses` (array, required)
- `pagination` (object, required)

## FAQ

### What does "Search Trustpilot companies" do?

Search Trustpilot businesses by name/keyword. Returns each company's identifyingName (the domain key used by get_company/get_reviews), TrustScore, stars, review count, location, contact and categories. Paginated.

### How do I automatically search Trustpilot companies on trustpilot.com?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/search_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/search_company

### Is there a trustpilot.com API to search Trustpilot companies?

You do not need one. "Search Trustpilot companies" drives the real trustpilot.com pages in a browser, so it works whether or not trustpilot.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns query, hasMore, businesses, pagination.

### Do I need to be logged in to trustpilot.com?

No. It only uses pages of trustpilot.com that are reachable without signing in.

### Does it change anything on trustpilot.com, or only read data?

It only reads. It looks things up on trustpilot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/search_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/search_company

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trustpilot.com/search_company
