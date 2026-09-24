# Create a task in a ClickUp list

Automatically create a task in a ClickUp list on app.clickup.com. Adds a task with the given name to a ClickUp list and confirms it afterwards, reporting the new task's identifier and link. A rehearsal mode fills the task in without submitting it, so the inputs can be checked before anything is created. This version sets the name only; description, priority, assignee and due date are left at the list's defaults.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/create_task`
- Updated: 2026-09-23 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/create_task`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/create_task
```

## Input

- `name` (string, required): The task name.
- `listId` (string, required): Numeric ClickUp list id, as returned by the ClickUp list lookup.
- `dry_run` (boolean, optional): Rehearse without creating anything. The task form is opened and the name and description are filled in and read back, then the run stops on the step before the one that submits it, so nothing reaches the list.
- `description` (string, optional): Optional task description. Plain text; line breaks become separate paragraphs. Written as pasted text, so a leading slash stays literal instead of opening ClickUp's command menu.
- `workspaceId` (string, optional): Numeric ClickUp workspace id. Supplying it skips a lookup step; omit it to let ClickUp resolve the default workspace.

## Output

- `name` (string, required)
- `dryRun` (boolean, required)
- `listId` (string, required)
- `created` (boolean, required)
- `listName` (string | null, required)
- `workspaceId` (string, required)
- `url` (string | null, optional)
- `taskId` (string | null, optional)
- `formReady` (boolean, optional)
- `accountUsed` (string | null, optional)
- `alreadyPresent` (boolean, optional)
- `verifiedOnPage` (boolean, optional)
- `existingMatches` (array, optional)
- `outcomeConfirmed` (boolean, optional)
- `descriptionApplied` (boolean, optional)
- `descriptionRequested` (boolean, optional)

## FAQ

### What does "Create a task in a ClickUp list" do?

Adds a task with the given name to a ClickUp list and confirms it afterwards, reporting the new task's identifier and link. A rehearsal mode fills the task in without submitting it, so the inputs can be checked before anything is created. This version sets the name only; description, priority, assignee and due date are left at the list's defaults.

### How do I automatically create a task in a ClickUp list on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/create_task, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/create_task

### Is there a app.clickup.com API to create a task in a ClickUp list?

You do not need one. "Create a task in a ClickUp list" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: listId, name. Optional: dry_run, description, workspaceId.

### What does it return?

It returns url, name, dryRun, listId, taskId, created, listName, formReady, accountUsed, workspaceId, alreadyPresent, verifiedOnPage, existingMatches, outcomeConfirmed, descriptionApplied, descriptionRequested.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It makes changes on app.clickup.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/create_task, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/create_task

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/create_task
