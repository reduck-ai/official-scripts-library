# Upload a file to Google Drive

Automatically upload a file to Google Drive on drive.google.com. Upload a file into a Google Drive folder, or into My Drive when no folder is given. Pass convert:true to store an Office/CSV/text file as a native Google Doc, Sheet or Slides instead of the raw file (the raw upload is moved to the Bin). Pass the bytes inline as base64 for small files, or point fileUrl at the file served over http://127.0.0.1:&lt;port&gt;/ on the machine running the browser for larger ones. Before reporting success it confirms a file absent beforehand AND carrying this call's own filename appeared: first in the folder view (up to 2 min), then, if the view lags, through Drive's own API (up to 1 more min), so a slow upload that did land is still reported with its real id. A filename already present in the destination is refused up front, because Drive stores a second, separate file under the same name. For the same reason a lost upload is reported as a failure rather than retried.

- Site: drive.google.com
- Address: `reduck/drive.google.com/upload_file`
- Updated: 2026-10-07 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/upload_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_file
```

## Input

- `mime` (string, optional): Content type to store. Defaults to application/octet-stream, or whatever the server reports for a fileUrl. Not used by the attachment input, which carries its own type.
- `convert` (boolean, optional): Store the upload as a native Google file instead of the raw file: .docx/.doc/.odt/.rtf/.txt/.html become a Google Doc, .xlsx/.xls/.ods/.csv/.tsv a Google Sheet, .pptx/.ppt/.odp Google Slides. The Google file takes the name without its extension and the raw upload is moved to the Bin. Refused for other file types. Needs a filename with an extension, so it does not work with the attachment input.
- `fileUrl` (string, optional): URL the browser's own machine can fetch the file from, e.g. http://127.0.0.1:8765/clip.mp4 (python3 -m http.server 8765 in the file's directory). Pass exactly one of attachment / fileBase64 / fileUrl.
- `filename` (string, optional): Name to store the file under in Drive, including its extension. Required for fileBase64 and fileUrl, and must not already exist in the destination folder. Not used when the attachment input is used: that route stores the file under the input's own name ('attachment'), which is inherent to the file-input convention.
- `folderId` (string, optional): Destination folder id, i.e. the <id> in drive.google.com/drive/folders/<id>. Omit to upload into the root of My Drive. Works for every route.
- `attachment` (string, optional): The file to upload, bound through the platform's own file channel and handed to Drive's own upload input. Preferred over fileBase64: it carries the bytes outside the argument payload, so there is no ~96KB ceiling and no need to serve the file over localhost. Note it is stored in Drive as 'attachment' — use fileBase64 or fileUrl when the stored name matters.
- `fileBase64` (string, optional): The file's bytes, base64-encoded. Suits files up to roughly 96KB; use the attachment input or fileUrl above that. Pass exactly one of attachment / fileBase64 / fileUrl.

## Output

- `fileId` (string, required): Drive id of the file the caller ends up with: the Google Doc/Sheet/Slides when converted, otherwise the uploaded file.
- `folderId` (string, required): Destination folder, or "root" for My Drive.
- `uploaded` (string, required): The name the resulting file carries in Drive.
- `verified` (string, required): How the upload was confirmed: named_row_appeared = a row absent before the upload and bearing this call's filename appeared in the folder view; api_listed = the view was slow, but Drive's API lists a file with this name in the destination, created during this run and absent beforehand. The script fails rather than reporting an unconfirmed upload.
- `converted` (boolean, required): True when the upload was turned into a native Google file.
- `bytes` (number | null, optional): Size of the payload uploaded.
- `mimeType` (string | null, optional): Mime type of the resulting file as Drive reports it (e.g. application/vnd.google-apps.document), when known.
- `webViewLink` (string | null, optional): Link to open the resulting file, when known.
- `originalFileId` (string | null, optional): When converted: id of the raw upload, now in the Bin.

## FAQ

### What does "Upload a file to Google Drive" do?

Upload a file into a Google Drive folder, or into My Drive when no folder is given. Pass convert:true to store an Office/CSV/text file as a native Google Doc, Sheet or Slides instead of the raw file (the raw upload is moved to the Bin). Pass the bytes inline as base64 for small files, or point fileUrl at the file served over http://127.0.0.1:&lt;port&gt;/ on the machine running the browser for larger ones. Before reporting success it confirms a file absent beforehand AND carrying this call's own filename appeared: first in the folder view (up to 2 min), then, if the view lags, through Drive's own API (up to 1 more min), so a slow upload that did land is still reported with its real id. A filename already present in the destination is refused up front, because Drive stores a second, separate file under the same name. For the same reason a lost upload is reported as a failure rather than retried.

### How do I automatically upload a file to Google Drive on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/upload_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_file

### Is there a drive.google.com API to upload a file to Google Drive?

You do not need one. "Upload a file to Google Drive" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Optional: mime, convert, fileUrl, filename, folderId, attachment, fileBase64.

### What does it return?

It returns bytes, fileId, folderId, mimeType, uploaded, verified, converted, webViewLink, originalFileId.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It makes changes on drive.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/upload_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/upload_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/upload_file
