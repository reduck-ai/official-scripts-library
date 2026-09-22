# Delete a Google Workspace user (Admin console)

Automatically delete a Google Workspace user (Admin console) on google.com. Deletes a user from the Google Admin console (Workspace) by their full primary email: locates their row in the directory's user list, opens their account page, and goes through the "delete" (not "suspend") path, confirming data-loss. Google purges unmigrated data ~20 days later. Irreversible-in-intent — use admin_create_user's counterpart carefully.

- Site: google.com
- Address: `reduck/google.com/admin_delete_user`
- Updated: 2026-08-10 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/admin_delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/admin_delete_user
```

## Input

- `email` (string, required): Full primary email of the user to delete, exactly as shown in the directory list, e.g. jdoe@example.com
- `adminEmail` (string, required): Already-signed-in Google Workspace admin account to select in the account chooser, e.g. admin@example.com

## Output

- `email` (string, required)
- `deleted` (boolean, required)
- `blocked` (string | null, optional): Set to reauth_required when Google demanded a password re-authentication, so nothing was deleted.

## FAQ

### What does "Delete a Google Workspace user (Admin console)" do?

Deletes a user from the Google Admin console (Workspace) by their full primary email: locates their row in the directory's user list, opens their account page, and goes through the "delete" (not "suspend") path, confirming data-loss. Google purges unmigrated data ~20 days later. Irreversible-in-intent — use admin_create_user's counterpart carefully.

### How do I automatically delete a Google Workspace user (Admin console) on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/admin_delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/admin_delete_user

### Is there a google.com API to delete a Google Workspace user (Admin console)?

You do not need one. "Delete a Google Workspace user (Admin console)" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: adminEmail, email.

### What does it return?

It returns email, blocked, deleted.

### Do I need to be logged in to google.com?

Yes. It acts as you on google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the google.com cookies saved by the Reduck extension.

### Does it change anything on google.com, or only read data?

It makes changes on google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/admin_delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/admin_delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/admin_delete_user
