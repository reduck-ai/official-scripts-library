# Upload a file to Google Drive

Automatically upload a file to Google Drive on drive.google.com. Upload one file into a Google Drive folder, or into My Drive when no folder is given, and return the stored file's id, name and link. Pass filename to choose the name it is stored under. When the folder already holds a file with that name, ifExists decides: fail (the default) uploads nothing, keepBoth adds a second file with a numbered name, replace adds a new version of the existing file and keeps its id.

- Site: drive.google.com
- Address: `reduck/drive.google.com/upload_file`
- Updated: 2026-10-22 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/upload_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_file
```

## Input

- `attachment` (string, required): The file to upload.
- `filename` (string, optional): Name to store the file under, with its extension. Defaults to the file's own name. Pass it when you send the file as bytes, because such a file arrives named "attachment".
- `folderId` (string, optional): Destination folder id, the <id> in drive.google.com/drive/folders/<id>. Omit to upload into the root of My Drive.
- `ifExists` (string, optional): What to do when the folder already holds a file with this name. fail uploads nothing and returns an error. keepBoth stores a second file, which Drive names with a number, for example "report (1).pdf". replace uploads a new version of the existing file, which keeps its id, link and sharing.

## Output

- `name` (string, required): The name the file has in Drive. With keepBoth, the numbered name Drive gave it.
- `fileId` (string, required): Id of the uploaded file. With replace, the id of the existing file that got a new version.
- `folderId` (string, required): Id of the folder the file is in.
- `mimeType` (string, required): The file's type in Drive.
- `replaced` (boolean, required): True when the upload became a new version of an existing file.
- `url` (string | null, optional): Link that opens the file.
- `sizeBytes` (number | null, optional): Size of the stored file.

## FAQ

### What does "Upload a file to Google Drive" do?

Upload one file into a Google Drive folder, or into My Drive when no folder is given, and return the stored file's id, name and link. Pass filename to choose the name it is stored under. When the folder already holds a file with that name, ifExists decides: fail (the default) uploads nothing, keepBoth adds a second file with a numbered name, replace adds a new version of the existing file and keeps its id.

### How do I automatically upload a file to Google Drive on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/upload_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_file

### Is there a drive.google.com API to upload a file to Google Drive?

You do not need one. "Upload a file to Google Drive" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Required: attachment. Optional: filename, folderId, ifExists.

### What does it return?

It returns url, name, fileId, folderId, mimeType, replaced, sizeBytes.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It makes changes on drive.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/upload_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/upload_file
