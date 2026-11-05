# Query a Notion database

Read the rows of a Notion database the signed-in account can open, in the order of one of its views, with every property's value by name (text, numbers, selects, multi-selects, dates, checkboxes, people, links to other rows), plus the database's properties and their options. Optionally keep only rows matching a text search. Takes the database's link or id; get it from search_pages.

- Site: app.notion.com
- Address: `reduck/app.notion.com/query_database`
- Updated: 2026-11-04 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/query_database`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/query_database
```

## Input

- `database` (string, required): Link to the database (https://app.notion.com/p/... or https://www.notion.so/...) or its id, with or without dashes.
- `view` (string, optional): View name or id whose filters and order to use. Leave it out for the database's first view.
- `limit` (integer, optional): Most rows to return, in the view's order.
- `search` (string, optional): Keep only rows whose text matches these words, as the search box of a database view does.

## Output

- `rows` (array, required)
- `view` (object, required)
- `total` (integer | null, required): How many rows the view holds (after search), when Notion says.
- `complete` (boolean, required): False when the view holds more rows than limit.
- `database` (object, required)
- `properties` (array, required)
- `views` (array, optional)

## FAQ

### What does "Query a Notion database" do?

Read the rows of a Notion database the signed-in account can open, in the order of one of its views, with every property's value by name (text, numbers, selects, multi-selects, dates, checkboxes, people, links to other rows), plus the database's properties and their options. Optionally keep only rows matching a text search. Takes the database's link or id; get it from search_pages.

### What information do I need to provide?

Required: database. Optional: view, limit, search.

### What does it return?

It returns rows, view, total, views, complete, database, properties.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/query_database, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/query_database

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/query_database
