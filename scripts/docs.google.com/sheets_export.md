# Sheets: export / download

Automatically export / download on docs.google.com. Save a Google Sheet as xlsx, ods or PDF, or one tab as CSV or TSV, and get back the file path.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_export`
- Updated: 2026-10-05 (v2)
- Author: Reduck AI (reduck)

## About

A finance team keeps expenses in one shared Google Sheet, a tab per month. At the start of October someone asks their agent for September, and it calls sheets_list_tabs, picks the gid listed next to the tab named Sept 2026, exports that tab as csv and gets back a local file path that goes straight into pandas or an accounting tool's CSV import. Run it again with xlsx or pdf and you have a dated copy of the whole workbook for the audit folder. The file comes from the spreadsheet's own export address, opened in your signed-in Chrome, so whatever your Google account can open is what gets downloaded, with no Cloud project or OAuth consent screen to set up. The catch is csv and tsv, which give one tab per run. A twelve-month workbook means twelve runs, or one xlsx that you split yourself. The pdf format returns the whole document.

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

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "url": "https://example.com/item/123",
  "path": "…",
  "filename": "…"
}
```

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

### Can I export a tab other than the first one as CSV?

Yes. Pass that tab's gid, which sheets_list_tabs returns and which also appears after gid= in the tab's URL. The default is 0, the gid of the tab the spreadsheet started with, so it may not be the tab you want if tabs were added, moved or deleted. The gid is ignored for xlsx, ods, pdf and zip.

### Which format keeps every tab?

xlsx, ods, pdf and zip export the whole document in one run. csv and tsv export a single tab as flat values, so use xlsx or ods when you need all tabs in one file. The code offers no option for page orientation or print range in the pdf.

### What happens with a very large spreadsheet?

The code sets no size limit of its own. It allows 30 seconds for the editor to load and another 30 seconds for the download to start, so a workbook that Google is slow to build can time out. Exporting only the tab you need as csv gives Google less to generate. Very large workbooks are untested.

### Do I get a file path or a link?

On a browser running on your own machine you get a local path and a filename. On managed cloud browsers there is no local disk, so you get a url instead of a path.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_export
