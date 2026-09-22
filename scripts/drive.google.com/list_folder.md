# List a Google Drive folder

Automatically list a Google Drive folder on drive.google.com. List the files and sub-folders directly inside a Google Drive folder, without recursing or downloading anything. Returns each item's id, name, type, size, last-modified date, owner and link. Omit folderId to list My Drive's root.

- Site: drive.google.com
- Address: `reduck/drive.google.com/list_folder`
- Updated: 2026-08-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/list_folder`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/list_folder
```

## Input

- `folderId` (string, optional): Google Drive folder id, i.e. the <id> in drive.google.com/drive/folders/<id>. Omit to list the root of My Drive.

## Output

- `url` (string, required)
- `count` (number, required): Folders plus files returned.
- `files` (array, required)
- `folders` (array, required)
- `complete` (boolean, required): False when the folder holds more rows than the listing payload described; missingMetadataFor then carries their ids.
- `folderId` (string, required): The folder listed, or "root" for My Drive.
- `missingMetadataFor` (array, optional)

## FAQ

### What does "List a Google Drive folder" do?

List the files and sub-folders directly inside a Google Drive folder, without recursing or downloading anything. Returns each item's id, name, type, size, last-modified date, owner and link. Omit folderId to list My Drive's root.

### How do I automatically list a Google Drive folder on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/list_folder, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/list_folder

### Is there a drive.google.com API to list a Google Drive folder?

You do not need one. "List a Google Drive folder" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Optional: folderId.

### What does it return?

It returns url, count, files, folders, complete, folderId, missingMetadataFor.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It only reads. It looks things up on drive.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/list_folder, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/list_folder

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/list_folder
