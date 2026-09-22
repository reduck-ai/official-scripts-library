# Sheets: write cells

Automatically write cells on docs.google.com. Write a 2D block of values into one tab of a Google Spreadsheet, top-left at startCell (clears the target rectangle first). Returns range, rows, cols, saved. Values are parsed per the spreadsheet locale ("1.5" in a FR sheet becomes 1 May; prefix ' to force text); leading = enters a formula; in-cell newlines are dropped; needs edit rights.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_write_cells`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_write_cells`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_write_cells
```

## Input

- `values` (array, required): 2D row-major block. null/"" leaves the (pre-cleared) cell empty. "=..." enters a formula.
- `spreadsheetId` (string, required): Spreadsheet id or any full docs.google.com spreadsheet URL
- `gid` (string | number, optional): Tab gid (from sheets_list_tabs). Default 0.
- `startCell` (string, optional): Top-left cell in A1 notation, e.g. "B2". Default "A1".

## Output

- `cols` (number, required)
- `rows` (number, required)
- `range` (string, required): A1 range that was written (and pre-cleared)
- `saved` (boolean, required): true once the editor's POST /save returned 200

## FAQ

### What does "Sheets: write cells" do?

Write a 2D block of values into one tab of a Google Spreadsheet, top-left at startCell (clears the target rectangle first). Returns range, rows, cols, saved. Values are parsed per the spreadsheet locale ("1.5" in a FR sheet becomes 1 May; prefix ' to force text); leading = enters a formula; in-cell newlines are dropped; needs edit rights.

### How do I automatically write cells on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_write_cells, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_write_cells

### Is there a docs.google.com API to write cells?

You do not need one. "Sheets: write cells" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: spreadsheetId, values. Optional: gid, startCell.

### What does it return?

It returns cols, rows, range, saved.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_write_cells, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_write_cells

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_write_cells
