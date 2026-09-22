# Download a Google Drive file

Automatically download a Google Drive file on drive.google.com. Download one Drive file by id to the device. Binary files (PDFs, images, video, Office documents) download as stored; Google-native Docs, Sheets and Slides are converted on the way out, so pass format to choose pdf, docx, xlsx, csv and the rest. Returns the saved filename and location. For a whole folder, list it first and call this once per file.

- Site: drive.google.com
- Address: `reduck/drive.google.com/download_file`
- Updated: 2026-08-25 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/download_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/download_file
```

## Input

- `fileId` (string, required): Drive file id, or any full Drive/Docs URL containing it.
- `gid` (string | number, optional): Tab gid, for csv/tsv exports of a Google Sheet. Defaults to the first tab.
- `format` (string, optional): Export format, for Google-native Docs/Sheets/Slides only. Defaults to pdf for documents and presentations, xlsx for spreadsheets. Ignored for files already stored as bytes.

## Output

- `kind` (string, required): How the file was fetched: stored bytes, or a converted export.
- `fileId` (string, required)
- `filename` (string, required): The saved file's real name.
- `url` (string | null, optional): Set instead of path on cloud browsers.
- `path` (string | null, optional): Location on the machine running the browser. Null on cloud browsers, where url is set instead.
- `format` (string | null, optional): The export format used, for Google-native files.
- `formatIgnored` (boolean, optional): True when a format was passed for a file stored as bytes, which downloads as-is.

## FAQ

### What does "Download a Google Drive file" do?

Download one Drive file by id to the device. Binary files (PDFs, images, video, Office documents) download as stored; Google-native Docs, Sheets and Slides are converted on the way out, so pass format to choose pdf, docx, xlsx, csv and the rest. Returns the saved filename and location. For a whole folder, list it first and call this once per file.

### How do I automatically download a Google Drive file on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/download_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/download_file

### Is there a drive.google.com API to download a Google Drive file?

You do not need one. "Download a Google Drive file" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Required: fileId. Optional: gid, format.

### What does it return?

It returns url, kind, path, fileId, format, filename, formatIgnored.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It only reads. It looks things up on drive.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/download_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/download_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/download_file
