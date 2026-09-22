# Create Google Drive folder

Automatically create Google Drive folder on drive.google.com. Create a new folder in Google Drive, optionally inside a given parent folder. Returns the new folder's id and name.

- Site: drive.google.com
- Address: `reduck/drive.google.com/create_folder`
- Updated: 2026-08-24 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/create_folder`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/create_folder
```

## Input

- `name` (string, required): Name for the new folder
- `parentId` (string, optional): Optional: the <id> in drive.google.com/drive/folders/<id> to create the folder inside. Omitted = created at the root of My Drive.

## Output

- `name` (string, required)
- `folderId` (string, required)
- `parentId` (string | null, optional): The folder the new folder was actually created in, read back from the listing it appeared in. Drive's own id for My Drive is returned when no parentId was given.

## FAQ

### What does "Create Google Drive folder" do?

Create a new folder in Google Drive, optionally inside a given parent folder. Returns the new folder's id and name.

### How do I automatically create Google Drive folder on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/create_folder, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/create_folder

### Is there a drive.google.com API to create Google Drive folder?

You do not need one. "Create Google Drive folder" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: parentId.

### What does it return?

It returns name, folderId, parentId.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It makes changes on drive.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/create_folder, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/create_folder

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/create_folder
