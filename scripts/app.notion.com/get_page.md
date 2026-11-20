# Read a Notion page

Automatically read a Notion page on app.notion.com. Read a Notion page the signed-in account can open: its title, its text, and its content in order as blocks (headings, paragraphs, to-dos with their state, list items, toggles, quotes, callouts, code, links to sub-pages and databases), nested blocks with their depth. Takes a page link or id; get ids from search_pages.

- Site: app.notion.com
- Address: `reduck/app.notion.com/get_page`
- Updated: 2026-11-19 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/get_page`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/get_page
```

## Input

- `page` (string, required): Link to the Notion page (https://app.notion.com/p/... or https://www.notion.so/...) or its id, with or without dashes.

## Output

- `id` (string, required)
- `url` (string, required)
- `text` (string, required): The page's text, one line per block, nested blocks indented.
- `title` (string | null, required)
- `blocks` (array, required)
- `lastEditedTime` (string | null, required)

## FAQ

### What does "Read a Notion page" do?

Read a Notion page the signed-in account can open: its title, its text, and its content in order as blocks (headings, paragraphs, to-dos with their state, list items, toggles, quotes, callouts, code, links to sub-pages and databases), nested blocks with their depth. Takes a page link or id; get ids from search_pages.

### How do I automatically read a Notion page on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/get_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/get_page

### Is there a app.notion.com API to read a Notion page?

You do not need one. "Read a Notion page" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: page.

### What does it return?

It returns id, url, text, title, blocks, lastEditedTime.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/get_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/get_page

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/get_page
