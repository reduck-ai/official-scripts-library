# Create a ClickUp Doc

Automatically create a ClickUp Doc on app.clickup.com. Creates a Doc in a ClickUp workspace with a title and, if you give one, a first page of text. Reports whether a doc of that name already existed and confirms the new doc by reading it back. A rehearsal mode checks the workspace and the name without creating anything.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/create_doc`
- Updated: 2026-09-24 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/create_doc`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/create_doc
```

## Input

- `name` (string, required): Title of the Doc. ClickUp also uses this as the name of its first page.
- `content` (string, optional): Optional text for the Doc's first page. Line breaks become separate paragraphs. Leave it out to create an empty Doc.
- `dry_run` (boolean, optional): When true the workspace is opened and the create control is checked, and the run stops before creating anything. Clicking that control is what creates the Doc in ClickUp, so there is no later step to stop at: created comes back false and docId is null.
- `workspaceId` (string, optional): Numeric ClickUp workspace id. Omit it to use the account's default workspace.

## Output

- `name` (string, required)
- `dryRun` (boolean, required)
- `created` (boolean, required)
- `workspaceId` (string, required)
- `url` (string | null, optional)
- `docId` (string | null, optional)
- `pageId` (string | null, optional)
- `accountUsed` (string | null, optional): The ClickUp account that performed the action, read from the session.
- `alreadyPresent` (boolean | null, optional): Whether a Doc of this name already existed in the workspace before the run. Null when ClickUp did not return the workspace's Doc list, so the answer is unknown rather than no.
- `verifiedOnPage` (boolean, optional): Whether the new Doc was re-opened after creation and its title, and text when one was given, were read back from ClickUp.
- `existingDocCount` (number | null, optional): How many Docs the workspace listed before the run, which is the basis for alreadyPresent.
- `createControlReady` (boolean, optional)

## FAQ

### What does "Create a ClickUp Doc" do?

Creates a Doc in a ClickUp workspace with a title and, if you give one, a first page of text. Reports whether a doc of that name already existed and confirms the new doc by reading it back. A rehearsal mode checks the workspace and the name without creating anything.

### How do I automatically create a ClickUp Doc on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/create_doc, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/create_doc

### Is there a app.clickup.com API to create a ClickUp Doc?

You do not need one. "Create a ClickUp Doc" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: content, dry_run, workspaceId.

### What does it return?

It returns url, name, docId, dryRun, pageId, created, accountUsed, workspaceId, alreadyPresent, verifiedOnPage, existingDocCount, createControlReady.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It makes changes on app.clickup.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/create_doc, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/create_doc

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/create_doc
