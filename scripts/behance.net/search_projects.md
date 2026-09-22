# Search Behance projects

Automatically search Behance projects on behance.net. Search Behance projects by keyword, returning title, url, owner, thumbnail, likes and views for each result.

- Site: behance.net
- Address: `reduck/behance.net/search_projects`
- Updated: 2026-08-26 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/behance.net/search_projects`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/behance.net/search_projects
```

## Input

- `query` (string, required): Search keywords, e.g. "logo design"
- `page` (integer, optional): Page number of results. Behance only serves page 1 to logged-out sessions: it silently re-serves page-1 content instead of paginating for anonymous visitors, so requesting a page above 1 throws rather than returning duplicate results. Omit, or pass 1.

## Output

- `results` (array, required)

## FAQ

### What does "Search Behance projects" do?

Search Behance projects by keyword, returning title, url, owner, thumbnail, likes and views for each result.

### How do I automatically search Behance projects on behance.net?

Ask an AI agent connected to Reduck to run reduck/behance.net/search_projects, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/behance.net/search_projects

### Is there a behance.net API to search Behance projects?

You do not need one. "Search Behance projects" drives the real behance.net pages in a browser, so it works whether or not behance.net offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns results.

### Do I need to be logged in to behance.net?

No. It only uses pages of behance.net that are reachable without signing in.

### Does it change anything on behance.net, or only read data?

It only reads. It looks things up on behance.net and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/behance.net/search_projects, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/behance.net/search_projects

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/behance.net/search_projects
