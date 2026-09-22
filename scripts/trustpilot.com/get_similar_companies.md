# Get Trustpilot similar companies

Automatically get Trustpilot similar companies on trustpilot.com. Get the companies Trustpilot lists as similar/competitors on a business profile (the "People also looked at" module). Returns each with its identifyingName (domain key), TrustScore, stars, review count and logo.

- Site: trustpilot.com
- Address: `reduck/trustpilot.com/get_similar_companies`
- Updated: 2026-08-15 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trustpilot.com/get_similar_companies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_similar_companies
```

## Input

- `domain` (string, required): Company domain key, e.g. "surfshark.com" (identifyingName from search_company).

## Output

- `domain` (string, required): Resolved identifyingName of the queried company.
- `companies` (array, required)

## FAQ

### What does "Get Trustpilot similar companies" do?

Get the companies Trustpilot lists as similar/competitors on a business profile (the "People also looked at" module). Returns each with its identifyingName (domain key), TrustScore, stars, review count and logo.

### How do I automatically get Trustpilot similar companies on trustpilot.com?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_similar_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_similar_companies

### Is there a trustpilot.com API to get Trustpilot similar companies?

You do not need one. "Get Trustpilot similar companies" drives the real trustpilot.com pages in a browser, so it works whether or not trustpilot.com offers an API for this.

### What information do I need to provide?

Required: domain.

### What does it return?

It returns domain, companies.

### Do I need to be logged in to trustpilot.com?

No. It only uses pages of trustpilot.com that are reachable without signing in.

### Does it change anything on trustpilot.com, or only read data?

It only reads. It looks things up on trustpilot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_similar_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_similar_companies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trustpilot.com/get_similar_companies
