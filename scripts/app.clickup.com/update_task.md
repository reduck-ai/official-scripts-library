# Update a ClickUp task's name, description or status

Automatically update a ClickUp task's name, description or status on app.clickup.com. Changes an existing ClickUp task's name, description or status, then reads the task back to confirm what actually changed. Values already matching are left alone. A rehearsal mode reports the current values and the change that would be made without altering anything.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/update_task`
- Updated: 2026-09-23 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/update_task`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/update_task
```

## Input

- `taskId` (string, required): The task's ClickUp id, as returned by the ClickUp task listing or by task creation.
- `name` (string, optional): New task name. Omit to leave it unchanged.
- `status` (string, optional): New status, given by the name the workspace uses for it, as the ClickUp task listing reports it (for example 'in progress'). Matching ignores case. A status the list does not offer is refused, and the available ones are named.
- `dry_run` (boolean, optional): Report the task's current values and the change that would be made, without altering anything. ClickUp saves a name or description as soon as the field loses focus, so this mode deliberately does not type into them; for a status it does check the requested one exists.
- `description` (string, optional): New task description, replacing whatever is there. Plain text; line breaks become separate paragraphs. Omit to leave it unchanged.
- `workspaceId` (string, optional): Numeric ClickUp workspace id. Supplying it skips a lookup step; omit it to let ClickUp resolve the default workspace.

## Output

- `dryRun` (boolean, required)
- `taskId` (string, required)
- `changed` (array, required)
- `workspaceId` (string, required)
- `url` (string, optional)
- `after` (object, optional)
- `before` (object, optional)
- `requested` (object, optional)
- `accountUsed` (string | null, optional)
- `alreadyMatched` (array, optional)
- `verifiedOnPage` (boolean, optional)
- `availableStatuses` (array, optional)

## FAQ

### What does "Update a ClickUp task's name, description or status" do?

Changes an existing ClickUp task's name, description or status, then reads the task back to confirm what actually changed. Values already matching are left alone. A rehearsal mode reports the current values and the change that would be made without altering anything.

### How do I automatically update a ClickUp task's name, description or status on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/update_task, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/update_task

### Is there a app.clickup.com API to update a ClickUp task's name, description or status?

You do not need one. "Update a ClickUp task's name, description or status" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: taskId. Optional: name, status, dry_run, description, workspaceId.

### What does it return?

It returns url, after, before, dryRun, taskId, changed, requested, accountUsed, workspaceId, alreadyMatched, verifiedOnPage, availableStatuses.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It makes changes on app.clickup.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/update_task, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/update_task

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/update_task
