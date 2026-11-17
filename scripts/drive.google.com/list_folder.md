# List a Google Drive folder

Automatically list a Google Drive folder on drive.google.com. List the files and sub-folders directly inside a Google Drive folder, without recursing or downloading anything. Returns each item's id, name, type, size, dates, owner and link, with folders and files in separate lists, all in one answer for folders of up to 1000 items; a larger folder fails. Omit folderId to list My Drive's root (its folderName is null). Pass authuser to choose the signed-in Google account. An empty folder returns empty lists. Fails when signed out, and on an id that is unknown or names a file.

- Site: drive.google.com
- Address: `reduck/drive.google.com/list_folder`
- Updated: 2026-11-16 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/list_folder`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/list_folder
```

## Input

- `authuser` (string, optional): Which signed-in Google account to use, by its email address or its index (0 for the first). Omit for Google's default account.
- `folderId` (string, optional): Google Drive folder id, the <id> in drive.google.com/drive/folders/<id>. Omit to list the root of My Drive.

## Output

- `count` (integer, required): Folders plus files.
- `files` (array, required)
- `folders` (array, required)
- `folderId` (string, required): The folder listed, or "root" for My Drive.
- `folderName` (string | null, required): The folder's name. Null for the root of My Drive.
- `url` (string, optional)

## FAQ

### What does "List a Google Drive folder" do?

List the files and sub-folders directly inside a Google Drive folder, without recursing or downloading anything. Returns each item's id, name, type, size, dates, owner and link, with folders and files in separate lists, all in one answer for folders of up to 1000 items; a larger folder fails. Omit folderId to list My Drive's root (its folderName is null). Pass authuser to choose the signed-in Google account. An empty folder returns empty lists. Fails when signed out, and on an id that is unknown or names a file.

### How do I automatically list a Google Drive folder on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/list_folder, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/list_folder

### Is there a drive.google.com API to list a Google Drive folder?

You do not need one. "List a Google Drive folder" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Optional: authuser, folderId.

### What does it return?

It returns url, count, files, folders, folderId, folderName.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It only reads. It looks things up on drive.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/list_folder, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/list_folder

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/list_folder
