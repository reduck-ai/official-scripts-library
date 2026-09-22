# Sheets: read tab values

Automatically read tab values on docs.google.com. Read one tab of a Google Spreadsheet as a 2D array of display values. Returns values (row-major, '' for empty and non-top-left merged cells), nRows, nCols. Values are display strings after formatting (a date may read as "1.5").

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_read_tab`
- Updated: 2026-08-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_read_tab`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_read_tab
```

## Input

- `spreadsheetId` (string, required): Spreadsheet id or any full docs.google.com spreadsheet URL
- `gid` (string | number, optional): Tab gid (from sheets_list_tabs). Default 0 (first tab).

## Output

- `nCols` (number, required)
- `nRows` (number, required)
- `values` (array, required): Row-major display values; '' for empty cells and non-top-left cells of merges

## FAQ

### What does "Sheets: read tab values" do?

Read one tab of a Google Spreadsheet as a 2D array of display values. Returns values (row-major, '' for empty and non-top-left merged cells), nRows, nCols. Values are display strings after formatting (a date may read as "1.5").

### How do I automatically read tab values on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_read_tab, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_read_tab

### Is there a docs.google.com API to read tab values?

You do not need one. "Sheets: read tab values" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: spreadsheetId. Optional: gid.

### What does it return?

It returns nCols, nRows, values.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

Unknown: its author has not declared whether it changes anything on docs.google.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_read_tab, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_read_tab

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_read_tab
