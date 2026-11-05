# Create a Notion page

Automatically create a Notion page on app.notion.com. Create a Notion page with a title and optional text, then read it back. Put it in your private pages, under another page, or in a database as a new row with property values by name (text, number, select, multi-select, date, checkbox; select options must already exist). Returns the new page's id and link. Get page and database ids from search_pages and their properties from query_database.

- Site: app.notion.com
- Address: `reduck/app.notion.com/create_page`
- Updated: 2026-11-04 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/create_page`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/create_page
```

## Input

- `title` (string, required): The page's title (for a database row: its title property).
- `text` (string, optional): Text for the page's body. Each line becomes its own paragraph, added as given.
- `parent` (string, optional): Link or id of the page to put it under, or of the database to add it to as a row. Leave it out for your private pages.
- `workspace` (string, optional): Workspace name or id for a private page, when the account belongs to several.
- `properties` (object, optional): For a database row: values by property name. Text takes a string, number a number, checkbox true or false, date an ISO date (2026-11-03), select an option name, multi-select a list of option names, person a list of workspace members' emails, relation a list of page links or ids, file a list of links (or {name, url}).

## Output

- `id` (string, required)
- `url` (string, required)
- `title` (string, required): The title as read back.
- `parentId` (string | null, required)
- `verified` (boolean, required): True when the page, read back, has the given title, text and properties.
- `parentType` (string, required): private, page or database.
- `text` (string, optional): The body as read back, one line per paragraph.
- `properties` (object, optional): For a database row: the values as read back, by property name.

## FAQ

### What does "Create a Notion page" do?

Create a Notion page with a title and optional text, then read it back. Put it in your private pages, under another page, or in a database as a new row with property values by name (text, number, select, multi-select, date, checkbox; select options must already exist). Returns the new page's id and link. Get page and database ids from search_pages and their properties from query_database.

### How do I automatically create a Notion page on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/create_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/create_page

### Is there a app.notion.com API to create a Notion page?

You do not need one. "Create a Notion page" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: title. Optional: text, parent, workspace, properties.

### What does it return?

It returns id, url, text, title, parentId, verified, parentType, properties.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It makes changes on app.notion.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/create_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/create_page

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/create_page
