# Download a Google Drive file

Automatically download a Google Drive file on drive.google.com. Download one Google Drive file by id, or by a Drive or Docs URL, to the machine running the browser. Files stored as bytes (PDFs, images, video, Office documents) download as they are; Google Docs, Sheets and Slides are exported, so pass format to choose pdf, docx, xlsx, csv and the rest. Returns the file's name and type in Drive and where it was saved. For a whole folder, list it first and call this once per file.

- Site: drive.google.com
- Address: `reduck/drive.google.com/download_file`
- Updated: 2026-10-13 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/download_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/download_file
```

## Input

- `fileId` (string, required): Drive file id, or any Drive or Docs URL that contains it.
- `gid` (string | number, optional): Tab id (the gid in the sheet URL), for a csv or tsv export of a Google Sheet. Omit for the first tab.
- `format` (string, optional): Export format for a Google Doc, Sheet or Slides file. Defaults to pdf for documents and presentations, xlsx for spreadsheets. Files stored as bytes download as they are and ignore it.

## Output

- `kind` (string, required): binary for a file stored as bytes, otherwise the Google type it was exported from.
- `name` (string, required): The file's name in Drive.
- `fileId` (string, required)
- `filename` (string, required): The name the file was saved under.
- `mimeType` (string, required): The file's type in Drive.
- `url` (string | null, optional): A link to the bytes, when they are not on the machine running the browser.
- `path` (string | null, optional): Where the file was saved on the machine running the browser.
- `format` (string | null, optional): The export format used, for a Google Doc, Sheet or Slides file.
- `formatIgnored` (boolean, optional): True when a format was passed for a file stored as bytes, which downloads as it is.

## FAQ

### What does "Download a Google Drive file" do?

Download one Google Drive file by id, or by a Drive or Docs URL, to the machine running the browser. Files stored as bytes (PDFs, images, video, Office documents) download as they are; Google Docs, Sheets and Slides are exported, so pass format to choose pdf, docx, xlsx, csv and the rest. Returns the file's name and type in Drive and where it was saved. For a whole folder, list it first and call this once per file.

### How do I automatically download a Google Drive file on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/download_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/download_file

### Is there a drive.google.com API to download a Google Drive file?

You do not need one. "Download a Google Drive file" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Required: fileId. Optional: gid, format.

### What does it return?

It returns url, kind, name, path, fileId, format, filename, mimeType, formatIgnored.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It only reads. It looks things up on drive.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/download_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/download_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/download_file
