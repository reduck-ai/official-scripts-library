# Sheets: add tab

Automatically add tab on docs.google.com. Add a tab to a Google Spreadsheet, optionally naming it in the same pass. Returns the new tab's gid and final name. Waits for the editor's save before resolving; needs edit rights.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_add_tab`
- Updated: 2026-08-28 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_add_tab`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_add_tab
```

## Input

- `spreadsheetId` (string, required): Spreadsheet id or any full docs.google.com spreadsheet URL
- `name` (string, optional): Optional name for the new tab, up to 100 characters and not already used in this spreadsheet. Omit to keep the default ("Sheet N"/"Feuille N").

## Output

- `gid` (string, required): gid of the new tab (use with sheets_read_tab / sheets_write_cells)
- `name` (string, required): Final tab name

## FAQ

### What does "Sheets: add tab" do?

Add a tab to a Google Spreadsheet, optionally naming it in the same pass. Returns the new tab's gid and final name. Waits for the editor's save before resolving; needs edit rights.

### How do I automatically add tab on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_add_tab, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_add_tab

### Is there a docs.google.com API to add tab?

You do not need one. "Sheets: add tab" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: spreadsheetId. Optional: name.

### What does it return?

It returns gid, name.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_add_tab, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_add_tab

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_add_tab
