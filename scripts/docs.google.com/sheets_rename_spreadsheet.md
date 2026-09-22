# Sheets: rename spreadsheet

Automatically rename spreadsheet on docs.google.com. Rename a Google Spreadsheet (the document title, not a tab). Returns the title as displayed after the rename. Waits for the rename to persist server-side before resolving; needs edit rights.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_rename_spreadsheet`
- Updated: 2026-08-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_rename_spreadsheet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_rename_spreadsheet
```

## Input

- `title` (string, required): New spreadsheet title
- `spreadsheetId` (string, required): Spreadsheet id or any full docs.google.com spreadsheet URL

## Output

- `title` (string, required): Title as displayed after the rename

## FAQ

### What does "Sheets: rename spreadsheet" do?

Rename a Google Spreadsheet (the document title, not a tab). Returns the title as displayed after the rename. Waits for the rename to persist server-side before resolving; needs edit rights.

### How do I automatically rename spreadsheet on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_rename_spreadsheet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_rename_spreadsheet

### Is there a docs.google.com API to rename spreadsheet?

You do not need one. "Sheets: rename spreadsheet" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: spreadsheetId, title.

### What does it return?

It returns title.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_rename_spreadsheet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_rename_spreadsheet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_rename_spreadsheet
