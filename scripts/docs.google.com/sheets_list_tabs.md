# Sheets: list tabs

Automatically list tabs on docs.google.com. List the tabs of a Google Spreadsheet. Returns sheets (name, gid) and the spreadsheet title. gid feeds sheets_read_tab / sheets_write_cells / the edit?gid= URL.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_list_tabs`
- Updated: 2026-08-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_list_tabs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_list_tabs
```

## Input

- `spreadsheetId` (string, required): Spreadsheet id (the /d/<id>/ part) or any full docs.google.com spreadsheet URL

## Output

- `title` (string | null, required): Spreadsheet title
- `sheets` (array, required)

## FAQ

### What does "Sheets: list tabs" do?

List the tabs of a Google Spreadsheet. Returns sheets (name, gid) and the spreadsheet title. gid feeds sheets_read_tab / sheets_write_cells / the edit?gid= URL.

### How do I automatically list tabs on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_list_tabs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_list_tabs

### Is there a docs.google.com API to list tabs?

You do not need one. "Sheets: list tabs" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: spreadsheetId.

### What does it return?

It returns title, sheets.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It only reads. It looks things up on docs.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_list_tabs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_list_tabs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_list_tabs
