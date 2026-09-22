# Move a Google Drive file to the Bin

Automatically move a Google Drive file to the Bin on drive.google.com. Moves a file to Drive's Bin (never a permanent delete), given just the file's id — its parent folder is resolved automatically.

- Site: drive.google.com
- Address: `reduck/drive.google.com/trash_file`
- Updated: 2026-08-28 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/trash_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/trash_file
```

## Input

- `fileId` (string, required): Drive file id to trash, i.e. the <id> in drive.google.com/file/d/<id>/view.

## Output

- `fileId` (string, required)
- `trashed` (boolean, required)

## FAQ

### What does "Move a Google Drive file to the Bin" do?

Moves a file to Drive's Bin (never a permanent delete), given just the file's id — its parent folder is resolved automatically.

### How do I automatically move a Google Drive file to the Bin on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/trash_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/trash_file

### Is there a drive.google.com API to move a Google Drive file to the Bin?

You do not need one. "Move a Google Drive file to the Bin" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Required: fileId.

### What does it return?

It returns fileId, trashed.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It makes changes on drive.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/trash_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/trash_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/trash_file
