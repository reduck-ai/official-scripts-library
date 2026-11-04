# Search Notion pages

Automatically search Notion pages on app.notion.com. Search the signed-in Notion workspace the way Notion's search does, by words in titles and content. Returns the total and, best matches first, each page or database with its id, title, type, link, parent, last edit time and the matching text. When the account belongs to several workspaces, pass the workspace. Pass a page's id to get_page, a database's id to query_database.

- Site: app.notion.com
- Address: `reduck/app.notion.com/search_pages`
- Updated: 2026-11-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/search_pages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/search_pages
```

## Input

- `query` (string, required): Words to search for in page titles and content, as in Notion's search.
- `limit` (integer, optional): Most results to return, best matches first.
- `workspace` (string, optional): Workspace name or id, when the account belongs to several. list_workspaces-style ids are in the error that asks for it.

## Output

- `total` (integer | null, required): How many matches Notion found; results holds at most limit of them.
- `results` (array, required)
- `workspace` (object, required)

## FAQ

### What does "Search Notion pages" do?

Search the signed-in Notion workspace the way Notion's search does, by words in titles and content. Returns the total and, best matches first, each page or database with its id, title, type, link, parent, last edit time and the matching text. When the account belongs to several workspaces, pass the workspace. Pass a page's id to get_page, a database's id to query_database.

### How do I automatically search Notion pages on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/search_pages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/search_pages

### Is there a app.notion.com API to search Notion pages?

You do not need one. "Search Notion pages" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit, workspace.

### What does it return?

It returns total, results, workspace.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/search_pages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/search_pages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/search_pages
