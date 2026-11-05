# Move a Notion page to the trash

Automatically move a Notion page to the trash on app.notion.com. Move a Notion page or database row to the trash, where it can be restored from for 30 days, or restore it from the trash with restore. Its sub-pages go with it. Returns whether the page is now in the trash, read back from Notion. Get page ids from search_pages or query_database.

- Site: app.notion.com
- Address: `reduck/app.notion.com/archive_page`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/archive_page`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/archive_page
```

## Input

- `page` (string, required): Link to the Notion page or database row, or its id.
- `restore` (boolean, optional): True to bring the page back from the trash instead.

## Output

- `id` (string, required)
- `title` (string | null, required)
- `changed` (boolean, required): False when the page was already where it was asked to be.
- `inTrash` (boolean, required): Whether the page is in the trash now, read back from Notion.

## FAQ

### What does "Move a Notion page to the trash" do?

Move a Notion page or database row to the trash, where it can be restored from for 30 days, or restore it from the trash with restore. Its sub-pages go with it. Returns whether the page is now in the trash, read back from Notion. Get page ids from search_pages or query_database.

### How do I automatically move a Notion page to the trash on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/archive_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/archive_page

### Is there a app.notion.com API to move a Notion page to the trash?

You do not need one. "Move a Notion page to the trash" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: page. Optional: restore.

### What does it return?

It returns id, title, changed, inTrash.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It makes changes on app.notion.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/archive_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/archive_page

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/archive_page
