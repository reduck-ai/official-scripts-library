# Upload a file to Google Drive

Automatically upload a file to Google Drive on drive.google.com. Upload a file into a Google Drive folder, or into My Drive when no folder is given. Pass the bytes inline as base64 for small files, or point fileUrl at the file served over http://127.0.0.1:&lt;port&gt;/ on the machine running the browser for larger ones. Before reporting success it waits for a row in the destination that was absent beforehand AND carries this call's own filename, so it cannot credit itself with a file another upload created; it returns that file's Drive id. A filename already present in the destination is refused up front, because a dropped file does NOT replace or get declined — Drive happily stores a second, separate file under the same name. For the same reason a lost upload is reported as a failure rather than retried: a re-drop would duplicate an upload that merely landed slowly.

- Site: drive.google.com
- Address: `reduck/drive.google.com/upload_file`
- Updated: 2026-09-22 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/upload_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_file
```

## Input

- `mime` (string, optional): Content type to store. Defaults to application/octet-stream, or whatever the server reports for a fileUrl. Not used by the attachment input, which carries its own type.
- `fileUrl` (string, optional): URL the browser's own machine can fetch the file from, e.g. http://127.0.0.1:8765/clip.mp4 (python3 -m http.server 8765 in the file's directory). Pass exactly one of attachment / fileBase64 / fileUrl.
- `filename` (string, optional): Name to store the file under in Drive, including its extension. Required for fileBase64 and fileUrl, and must not already exist in the destination folder. Not used when the attachment input is used: that route stores the file under the input's own name ('attachment'), which is inherent to the file-input convention.
- `folderId` (string, optional): Destination folder id, i.e. the <id> in drive.google.com/drive/folders/<id>. Omit to upload into the root of My Drive. Works for every route.
- `attachment` (string, optional): The file to upload, bound through the platform's own file channel and handed to Drive's own upload input. Preferred over fileBase64: it carries the bytes outside the argument payload, so there is no ~96KB ceiling and no need to serve the file over localhost. Note it is stored in Drive as 'attachment' — use fileBase64 or fileUrl when the stored name matters.
- `fileBase64` (string, optional): The file's bytes, base64-encoded. Suits files up to roughly 96KB; use the attachment input or fileUrl above that. Pass exactly one of attachment / fileBase64 / fileUrl.

## Output

- `fileId` (string, required): Drive file id of the newly created file.
- `folderId` (string, required): Destination folder, or "root" for My Drive.
- `uploaded` (string, required): The filename as Drive stored it.
- `verified` (string, required): Always named_row_appeared: a row absent from the folder before the upload AND bearing this call's own filename. The script fails rather than reporting an unconfirmed upload, and will not credit itself with a file another run created.
- `bytes` (number | null, optional): Size of the payload uploaded.

## FAQ

### What does "Upload a file to Google Drive" do?

Upload a file into a Google Drive folder, or into My Drive when no folder is given. Pass the bytes inline as base64 for small files, or point fileUrl at the file served over http://127.0.0.1:&lt;port&gt;/ on the machine running the browser for larger ones. Before reporting success it waits for a row in the destination that was absent beforehand AND carries this call's own filename, so it cannot credit itself with a file another upload created; it returns that file's Drive id. A filename already present in the destination is refused up front, because a dropped file does NOT replace or get declined — Drive happily stores a second, separate file under the same name. For the same reason a lost upload is reported as a failure rather than retried: a re-drop would duplicate an upload that merely landed slowly.

### How do I automatically upload a file to Google Drive on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/upload_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_file

### Is there a drive.google.com API to upload a file to Google Drive?

You do not need one. "Upload a file to Google Drive" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Optional: mime, fileUrl, filename, folderId, attachment, fileBase64.

### What does it return?

It returns bytes, fileId, folderId, uploaded, verified.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It makes changes on drive.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/upload_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/upload_file
