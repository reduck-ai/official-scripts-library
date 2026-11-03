# Search n8n workflow templates

Automatically search n8n workflow templates on n8n.io. Search the n8n workflow template gallery (n8n.io/workflows) by text and category, sorted by relevance, popularity (views) or date, one page at a time. Without a query it lists every template, so sort popular gives the most viewed templates of the gallery. Returns the total number of matches, whether a next page exists, and per template its id, name, url, views, price and purchase link (price 0 or null for a free template), creation date, creator, the apps it uses and its description, plus the 10 categories with the most matches and their counts. A search with no match, or a page past the end, returns an empty list. Pass a template's id to n8n.io/get_template for its nodes, complexity and workflow JSON.

- Site: n8n.io
- Address: `reduck/n8n.io/search_templates`
- Updated: 2026-11-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/n8n.io/search_templates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/n8n.io/search_templates
```

## Input

- `page` (integer, optional)
- `sort` (string, optional): relevance: best text match first; popular: most viewed first; recent: newest first. Leave it out for the gallery's own order.
- `query` (string, optional): Text to search in the templates (an app, a task, a role). Leave it out to list every template.
- `category` (string, optional): A category name as the gallery writes it, e.g. "Sales", "Lead Generation", "AI". The `categories` of a search's output lists names with their counts.
- `pageSize` (integer, optional): Templates per page. The gallery shows 9; the most it answers is 250.

## Output

- `page` (integer, required)
- `total` (integer, required)
- `pageSize` (integer, required)
- `templates` (array, required)
- `categories` (array, required)
- `hasNextPage` (boolean, required)

## FAQ

### What does "Search n8n workflow templates" do?

Search the n8n workflow template gallery (n8n.io/workflows) by text and category, sorted by relevance, popularity (views) or date, one page at a time. Without a query it lists every template, so sort popular gives the most viewed templates of the gallery. Returns the total number of matches, whether a next page exists, and per template its id, name, url, views, price and purchase link (price 0 or null for a free template), creation date, creator, the apps it uses and its description, plus the 10 categories with the most matches and their counts. A search with no match, or a page past the end, returns an empty list. Pass a template's id to n8n.io/get_template for its nodes, complexity and workflow JSON.

### How do I automatically search n8n workflow templates on n8n.io?

Ask an AI agent connected to Reduck to run reduck/n8n.io/search_templates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/n8n.io/search_templates

### Is there a n8n.io API to search n8n workflow templates?

You do not need one. "Search n8n workflow templates" drives the real n8n.io pages in a browser, so it works whether or not n8n.io offers an API for this.

### What information do I need to provide?

Optional: page, sort, query, category, pageSize.

### What does it return?

It returns page, total, pageSize, templates, categories, hasNextPage.

### Do I need to be logged in to n8n.io?

No. It only uses pages of n8n.io that are reachable without signing in.

### Does it change anything on n8n.io, or only read data?

It only reads. It looks things up on n8n.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/n8n.io/search_templates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/n8n.io/search_templates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/n8n.io/search_templates
