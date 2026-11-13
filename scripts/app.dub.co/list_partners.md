# List Dub program partners

Automatically list Dub program partners on app.dub.co. List the partners of a Dub Partners program with their status, group, country, partner links and results (clicks, leads, conversions, sales revenue, commissions), as the Partners page of the workspace shows them. Filter by status (approved, invited, pending, rejected, declined, deactivated, banned, archived) or by search text, and page through with page and page_size. Amounts are in cents. Without a status or search, it returns the approved partners, which is what the page opens on. Requires being signed in to Dub with access to the workspace.

- Site: app.dub.co
- Address: `reduck/app.dub.co/list_partners`
- Updated: 2026-11-12 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.dub.co/list_partners`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.dub.co/list_partners
```

## Input

- `page` (integer, optional): 1-based page number. Use next_page from the previous answer.
- `search` (string, optional): Search text, matched against partner name, email and links like the page's search box does.
- `status` (string, optional): Only the partners with this status. Leave out for the page's default view: the approved partners, or every status when search is given.
- `page_size` (integer, optional): Partners per page. Dub allows at most 100.
- `workspace_slug` (string, optional): Slug of the Dub workspace, as it appears in app.dub.co/<slug>. Leave out to use the workspace Dub opens by default.

## Output

- `page` (integer, required)
- `total` (integer, required): Partners matching the filter, over all pages.
- `search` (string | null, required)
- `status` (string | null, required): The status filter the page applied. Null when a search covered every status.
- `complete` (boolean, required): True when this page reaches the last matching partner.
- `partners` (array, required)
- `next_page` (integer | null, required): The next page number, or null on the last page.
- `page_size` (integer, required)
- `workspace` (string, required): Slug of the workspace that was read.

## FAQ

### What does "List Dub program partners" do?

List the partners of a Dub Partners program with their status, group, country, partner links and results (clicks, leads, conversions, sales revenue, commissions), as the Partners page of the workspace shows them. Filter by status (approved, invited, pending, rejected, declined, deactivated, banned, archived) or by search text, and page through with page and page_size. Amounts are in cents. Without a status or search, it returns the approved partners, which is what the page opens on. Requires being signed in to Dub with access to the workspace.

### How do I automatically list Dub program partners on app.dub.co?

Ask an AI agent connected to Reduck to run reduck/app.dub.co/list_partners, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.dub.co/list_partners

### Is there a app.dub.co API to list Dub program partners?

You do not need one. "List Dub program partners" drives the real app.dub.co pages in a browser, so it works whether or not app.dub.co offers an API for this.

### What information do I need to provide?

Optional: page, search, status, page_size, workspace_slug.

### What does it return?

It returns page, total, search, status, complete, partners, next_page, page_size, workspace.

### Do I need to be logged in to app.dub.co?

Yes. It acts as you on app.dub.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.dub.co cookies saved by the Reduck extension.

### Does it change anything on app.dub.co, or only read data?

It only reads. It looks things up on app.dub.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.dub.co/list_partners, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.dub.co/list_partners

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.dub.co/list_partners
