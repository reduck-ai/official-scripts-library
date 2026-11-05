# Update a Notion page

Automatically update a Notion page on app.notion.com. Change a Notion page's title, or the property values of a database row by property name (text, number, select, multi-select, date, checkbox; null empties a property), then read it back. Properties you leave out keep their values; a value that is already set is not sent again. Get page ids from search_pages or query_database, and a database's properties and options from query_database.

- Site: app.notion.com
- Address: `reduck/app.notion.com/update_page`
- Updated: 2026-11-04 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/update_page`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/update_page
```

## Input

- `page` (string, required): Link to the Notion page or database row, or its id.
- `title` (string, optional): New title.
- `properties` (object, optional): For a database row: new values by property name; null empties one. Text takes a string, number a number, checkbox true or false, date an ISO date (2026-11-03), select or status an option name, multi-select a list of option names, person a list of workspace members' emails, relation a list of page links or ids, file a list of links (or {name, url}). Lists replace the current value.

## Output

- `id` (string, required)
- `url` (string, required)
- `title` (string, required): The title as read back.
- `changed` (array, required): Names of what changed (title or property names); values already set are left out.
- `verified` (boolean, required): True when the page, read back, has every value given.
- `properties` (object, optional): For a database row: the changed properties as read back, by name.

## FAQ

### What does "Update a Notion page" do?

Change a Notion page's title, or the property values of a database row by property name (text, number, select, multi-select, date, checkbox; null empties a property), then read it back. Properties you leave out keep their values; a value that is already set is not sent again. Get page ids from search_pages or query_database, and a database's properties and options from query_database.

### How do I automatically update a Notion page on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/update_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/update_page

### Is there a app.notion.com API to update a Notion page?

You do not need one. "Update a Notion page" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: page. Optional: title, properties.

### What does it return?

It returns id, url, title, changed, verified, properties.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It makes changes on app.notion.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/update_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/update_page

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/update_page
