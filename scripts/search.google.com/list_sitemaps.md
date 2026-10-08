# List Google Search Console sitemaps

Automatically list Google Search Console sitemaps on search.google.com. Lists the sitemaps submitted for a Google Search Console property, with when each was submitted and last read, its fetch status, and how many pages and videos Google discovered in it. Takes the property as listed by search.google.com/list_properties.

- Site: search.google.com
- Address: `reduck/search.google.com/list_sitemaps`
- Updated: 2026-10-07 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/search.google.com/list_sitemaps`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/search.google.com/list_sitemaps
```

## Input

- `siteUrl` (string, required): The property, exactly as search.google.com/list_properties returns it: a URL prefix such as https://example.com/ or sc-domain:example.com.

## Output

- `siteUrl` (string, required)
- `sitemaps` (array, required): Submitted sitemaps, as in the Sitemaps report. Empty when none have been submitted.

## FAQ

### What does "List Google Search Console sitemaps" do?

Lists the sitemaps submitted for a Google Search Console property, with when each was submitted and last read, its fetch status, and how many pages and videos Google discovered in it. Takes the property as listed by search.google.com/list_properties.

### How do I automatically list Google Search Console sitemaps on search.google.com?

Ask an AI agent connected to Reduck to run reduck/search.google.com/list_sitemaps, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.google.com/list_sitemaps

### Is there a search.google.com API to list Google Search Console sitemaps?

You do not need one. "List Google Search Console sitemaps" drives the real search.google.com pages in a browser, so it works whether or not search.google.com offers an API for this.

### What information do I need to provide?

Required: siteUrl.

### What does it return?

It returns siteUrl, sitemaps.

### Do I need to be logged in to search.google.com?

Yes. It acts as you on search.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the search.google.com cookies saved by the Reduck extension.

### Does it change anything on search.google.com, or only read data?

It only reads. It looks things up on search.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/search.google.com/list_sitemaps, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.google.com/list_sitemaps

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/search.google.com/list_sitemaps
