# Get Similarweb competitors and similar sites

Automatically get Similarweb competitors and similar sites on similarweb.com. Read a website's competitors / similar sites from its public Similarweb overview page: competitor domain, affinity percent, category and category rank. No login required. Returns the ~10 competitors the anonymous page renders; the section's "See all competitors" expander leads to gated Similarweb product pages, so that is the anonymous ceiling. available:false means Similarweb has no report for that domain.

- Site: similarweb.com
- Address: `reduck/similarweb.com/get_competitors`
- Updated: 2026-09-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/similarweb.com/get_competitors`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/similarweb.com/get_competitors
```

## Input

- `domain` (string, required): Website domain, e.g. "spotify.com" or "notion.so". A full URL or a leading www. is accepted and normalised to the bare host.

## Output

- `domain` (string, required): The normalised domain the report was requested for.
- `available` (boolean, required): False when Similarweb has no report for this domain (it redirects to /website/ with no domain segment) — an expected outcome for small or unknown sites, not an error.
- `competitors` (array, required): Empty array is a legitimate outcome: available:false, or a report whose competitors section renders no rows.
- `competitorCount` (integer, required): Number of competitors returned — how many the anonymous page rendered, not the total Similarweb knows.

## FAQ

### What does "Get Similarweb competitors and similar sites" do?

Read a website's competitors / similar sites from its public Similarweb overview page: competitor domain, affinity percent, category and category rank. No login required. Returns the ~10 competitors the anonymous page renders; the section's "See all competitors" expander leads to gated Similarweb product pages, so that is the anonymous ceiling. available:false means Similarweb has no report for that domain.

### How do I automatically get Similarweb competitors and similar sites on similarweb.com?

Ask an AI agent connected to Reduck to run reduck/similarweb.com/get_competitors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/similarweb.com/get_competitors

### Is there a similarweb.com API to get Similarweb competitors and similar sites?

You do not need one. "Get Similarweb competitors and similar sites" drives the real similarweb.com pages in a browser, so it works whether or not similarweb.com offers an API for this.

### What information do I need to provide?

Required: domain.

### What does it return?

It returns domain, available, competitors, competitorCount.

### Do I need to be logged in to similarweb.com?

No. It only uses pages of similarweb.com that are reachable without signing in.

### Does it change anything on similarweb.com, or only read data?

It only reads. It looks things up on similarweb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/similarweb.com/get_competitors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/similarweb.com/get_competitors

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/similarweb.com/get_competitors
