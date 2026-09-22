# Share a Google Drive file

Automatically share a Google Drive file on drive.google.com. Grant, update, or revoke a specific email's access to a Drive file (with a viewer/commenter/editor role), or toggle the file's general link-sharing mode between restricted and anyone-with-the-link.

- Site: drive.google.com
- Address: `reduck/drive.google.com/share_file`
- Updated: 2026-08-24 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/share_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/share_file
```

## Input

- `fileId` (string, required): Drive file id, i.e. the <id> in drive.google.com/file/d/<id>/view.
- `role` (string, optional): Access level to grant/update when email is given. Ignored when revoke is true.
- `email` (string, optional): Email to grant, update, or revoke access for. Combine with role to grant/update; combine with revoke:true to remove access.
- `notify` (boolean, optional): Whether to email the person when granting access. Defaults to Drive's own default (checked/true). Ignored for revoke/linkSharing.
- `revoke` (boolean, optional): When true (with email), removes that person's access instead of granting/updating it.
- `linkSharing` (string, optional): Sets the file's general link-sharing mode. Provide this instead of email/role/revoke.

## Output

- `action` (string, required)
- `fileId` (string, required)
- `confirmed` (boolean, required): True if the site's own response confirmed the change (a permission id for grant, 204/200 for revoke, the new access level for link sharing). Also true on a no-op linkSharing call, where alreadySet reports the mode was already in force so no request was needed.
- `role` (string | null, optional)
- `email` (string | null, optional)
- `alreadySet` (boolean | null, optional): linkSharing only, and always present there: true when the requested mode was already the file's current one, so nothing changed and Drive issued no request; false when this call actually changed it. Absent for grant and revoke.
- `linkSharing` (string | null, optional)

## FAQ

### What does "Share a Google Drive file" do?

Grant, update, or revoke a specific email's access to a Drive file (with a viewer/commenter/editor role), or toggle the file's general link-sharing mode between restricted and anyone-with-the-link.

### How do I automatically share a Google Drive file on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/share_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/share_file

### Is there a drive.google.com API to share a Google Drive file?

You do not need one. "Share a Google Drive file" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Required: fileId. Optional: role, email, notify, revoke, linkSharing.

### What does it return?

It returns role, email, action, fileId, confirmed, alreadySet, linkSharing.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It makes changes on drive.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/share_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/share_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/share_file
