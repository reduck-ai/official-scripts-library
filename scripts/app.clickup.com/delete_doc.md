# Delete a ClickUp Doc

Automatically delete a ClickUp Doc on app.clickup.com. Moves a ClickUp Doc to the workspace trash, taking the Doc's link or its id. Reports the Doc's title before removing it and confirms afterwards that it has left the workspace's Doc list. A rehearsal mode checks the Doc and the delete control without removing anything.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/delete_doc`
- Updated: 2026-09-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/delete_doc`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/delete_doc
```

## Input

- `doc` (string, required): The Doc to delete: its ClickUp link, or just its id (for example 2kyqw87p-1055).
- `dry_run` (boolean, optional): When true the Doc is located and the delete control is checked, and the run stops before removing anything. Clicking that control is what deletes the Doc in ClickUp, so there is no later step to stop at: deleted comes back false.
- `workspaceId` (string, optional): Numeric ClickUp workspace id. Only needed when the Doc is given as a bare id; omit it to use the account's default workspace.

## Output

- `docId` (string, required)
- `dryRun` (boolean, required)
- `deleted` (boolean, required)
- `workspaceId` (string, required)
- `url` (string | null, optional)
- `name` (string | null, optional): The Doc's title as it stood before this run, carried out so the caller can see which Doc was acted on. Null when the Doc has no title.
- `accountUsed` (string | null, optional): The ClickUp account that performed the action, read from the session.
- `docCountAfter` (number | null, optional)
- `docCountBefore` (number | null, optional)
- `verifiedAbsent` (boolean, optional): Whether the workspace's Doc list was read again after the deletion and no longer carried this id.
- `deleteControlReady` (boolean, optional)

## FAQ

### What does "Delete a ClickUp Doc" do?

Moves a ClickUp Doc to the workspace trash, taking the Doc's link or its id. Reports the Doc's title before removing it and confirms afterwards that it has left the workspace's Doc list. A rehearsal mode checks the Doc and the delete control without removing anything.

### How do I automatically delete a ClickUp Doc on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/delete_doc, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/delete_doc

### Is there a app.clickup.com API to delete a ClickUp Doc?

You do not need one. "Delete a ClickUp Doc" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: doc. Optional: dry_run, workspaceId.

### What does it return?

It returns url, name, docId, dryRun, deleted, accountUsed, workspaceId, docCountAfter, docCountBefore, verifiedAbsent, deleteControlReady.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It makes changes on app.clickup.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/delete_doc, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/delete_doc

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/delete_doc
