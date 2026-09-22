# Sheets: clear range

Automatically clear range on docs.google.com. Clear the values of an A1 range in one tab of a Google Spreadsheet (values only, formatting stays). Returns range and cleared. Clearing an already-empty range is a safe no-op; needs edit rights.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_clear_range`
- Updated: 2026-08-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_clear_range`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_clear_range
```

## Input

- `range` (string, required): A1 range accepted by the name box: "B2:D10", "C3", "A:C", "2:5", or a named range
- `spreadsheetId` (string, required): Spreadsheet id or any full docs.google.com spreadsheet URL
- `gid` (string | number, optional): Tab gid (from sheets_list_tabs). Default 0.

## Output

- `range` (string, required)
- `cleared` (boolean, required)

## FAQ

### What does "Sheets: clear range" do?

Clear the values of an A1 range in one tab of a Google Spreadsheet (values only, formatting stays). Returns range and cleared. Clearing an already-empty range is a safe no-op; needs edit rights.

### How do I automatically clear range on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_clear_range, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_clear_range

### Is there a docs.google.com API to clear range?

You do not need one. "Sheets: clear range" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: spreadsheetId, range. Optional: gid.

### What does it return?

It returns range, cleared.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_clear_range, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_clear_range

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_clear_range
