# Sheets: export / download

Automatically export / download on docs.google.com. Download a Google Spreadsheet to a local file in your chosen format. Returns path (or url on cloud browsers) and filename. xlsx/ods/pdf/zip export the whole doc; csv/tsv export a single tab (pass gid).

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_export`
- Updated: 2026-08-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_export`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_export
```

## Input

- `spreadsheetId` (string, required): Spreadsheet id or any full docs.google.com spreadsheet URL
- `gid` (string | number, optional): Tab gid for csv/tsv (from sheets_list_tabs). Default 0. Ignored for whole-document formats.
- `format` (string, optional): Default xlsx. csv/tsv export a single tab (see gid).

## Output

- `filename` (string, required)
- `url` (string | null, optional): Set instead of path on managed (cloud) browsers
- `path` (string | null, optional): Local path on the agent machine

## FAQ

### What does "Sheets: export / download" do?

Download a Google Spreadsheet to a local file in your chosen format. Returns path (or url on cloud browsers) and filename. xlsx/ods/pdf/zip export the whole doc; csv/tsv export a single tab (pass gid).

### How do I automatically export / download on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_export, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_export

### Is there a docs.google.com API to export / download?

You do not need one. "Sheets: export / download" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: spreadsheetId. Optional: gid, format.

### What does it return?

It returns url, path, filename.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It only reads. It looks things up on docs.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_export, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_export

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_export
