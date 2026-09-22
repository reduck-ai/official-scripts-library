# Sheets: delete tab

Automatically delete tab on docs.google.com. Delete one tab of a Google Spreadsheet by gid. Returns deletedGid and remainingTabs (names left). The sheet's data goes with it (recover via Undo / Drive history); an unknown gid throws rather than risk deleting the wrong sheet; needs edit rights.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_delete_tab`
- Updated: 2026-08-28 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_delete_tab`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_delete_tab
```

## Input

- `gid` (string | number, required): gid of the tab to delete (from sheets_list_tabs)
- `spreadsheetId` (string, required): Spreadsheet id or any full docs.google.com spreadsheet URL

## Output

- `deletedGid` (string, required)
- `remainingTabs` (array, required): Names of the tabs left after deletion

## FAQ

### What does "Sheets: delete tab" do?

Delete one tab of a Google Spreadsheet by gid. Returns deletedGid and remainingTabs (names left). The sheet's data goes with it (recover via Undo / Drive history); an unknown gid throws rather than risk deleting the wrong sheet; needs edit rights.

### How do I automatically delete tab on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_delete_tab, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_delete_tab

### Is there a docs.google.com API to delete tab?

You do not need one. "Sheets: delete tab" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: spreadsheetId, gid.

### What does it return?

It returns deletedGid, remainingTabs.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_delete_tab, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_delete_tab

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_delete_tab
