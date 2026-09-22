# Upload a file to Google Drive (file input)

Automatically upload a file to Google Drive (file input) on drive.google.com. Uploads a file into the root of Google Drive using the file-picker flow behind Drive's own upload button, then confirms a new item bearing that upload appears in the file list.

- Site: drive.google.com
- Address: `reduck/drive.google.com/upload_via_uploadfile`
- Updated: 2026-09-21 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/upload_via_uploadfile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_via_uploadfile
```

## Input

- `test-upload.pdf` (string, required)

## Output

- `fileId` (string, required): Drive file id of the uploaded file, read from the new row.
- `filename` (string, required): The name Drive stored the upload under, read from the new row rather than assumed from the input's declared key.

## FAQ

### What does "Upload a file to Google Drive (file input)" do?

Uploads a file into the root of Google Drive using the file-picker flow behind Drive's own upload button, then confirms a new item bearing that upload appears in the file list.

### How do I automatically upload a file to Google Drive (file input) on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/upload_via_uploadfile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_via_uploadfile

### Is there a drive.google.com API to upload a file to Google Drive (file input)?

You do not need one. "Upload a file to Google Drive (file input)" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Required: test-upload.pdf.

### What does it return?

It returns fileId, filename.

### Do I need to be logged in to drive.google.com?

No. It only uses pages of drive.google.com that are reachable without signing in.

### Does it change anything on drive.google.com, or only read data?

It makes changes on drive.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/upload_via_uploadfile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_via_uploadfile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/upload_via_uploadfile
