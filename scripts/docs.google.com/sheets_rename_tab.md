# Sheets: rename tab

Automatically rename tab on docs.google.com. Rename one tab of a Google Spreadsheet by gid. Returns the gid and the name as displayed after the rename. If no tab in the spreadsheet has that gid it stops with a clear error instead of renaming a different tab. Waits for the editor's save before resolving; needs edit rights.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_rename_tab`
- Updated: 2026-08-13 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_rename_tab`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_rename_tab
```

## Input

- `gid` (string | number, required): gid of the tab to rename (from sheets_list_tabs)
- `name` (string, required): New tab name
- `spreadsheetId` (string, required): Spreadsheet id or any full docs.google.com spreadsheet URL

## Output

- `gid` (string, required)
- `name` (string, required): Name as displayed after the rename

## FAQ

### What does "Sheets: rename tab" do?

Rename one tab of a Google Spreadsheet by gid. Returns the gid and the name as displayed after the rename. If no tab in the spreadsheet has that gid it stops with a clear error instead of renaming a different tab. Waits for the editor's save before resolving; needs edit rights.

### How do I automatically rename tab on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_rename_tab, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_rename_tab

### Is there a docs.google.com API to rename tab?

You do not need one. "Sheets: rename tab" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: spreadsheetId, gid, name.

### What does it return?

It returns gid, name.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_rename_tab, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_rename_tab

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_rename_tab
