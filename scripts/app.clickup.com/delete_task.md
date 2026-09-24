# Delete a task from a ClickUp list

Automatically delete a task from a ClickUp list on app.clickup.com. Deletes one task from a ClickUp list and confirms it is gone afterwards. ClickUp moves a deleted task to the workspace trash, where it can still be restored. A rehearsal mode locates the task and reports what would be deleted without removing it.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/delete_task`
- Updated: 2026-09-23 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/delete_task`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/delete_task
```

## Input

- `listId` (string, required): Numeric ClickUp list id holding the task. The ClickUp task listing returns it alongside each task.
- `taskId` (string, required): The task's ClickUp id, as returned by the ClickUp task listing or by task creation.
- `dry_run` (boolean, optional): Rehearse without deleting. The task is located and reported, then the run stops on the step before the one that removes it.
- `workspaceId` (string, optional): Numeric ClickUp workspace id. Supplying it skips a lookup step; omit it to let ClickUp resolve the default workspace.

## Output

- `dryRun` (boolean, required)
- `listId` (string, required)
- `taskId` (string, required)
- `deleted` (boolean, required)
- `workspaceId` (string, required)
- `listName` (string | null, optional)
- `taskName` (string | null, optional)
- `tasksAfter` (integer | null, optional)
- `accountUsed` (string | null, optional)
- `tasksBefore` (integer, optional)
- `movedToTrash` (boolean, optional)
- `verifiedGone` (boolean, optional)
- `outcomeConfirmed` (boolean, optional)

## FAQ

### What does "Delete a task from a ClickUp list" do?

Deletes one task from a ClickUp list and confirms it is gone afterwards. ClickUp moves a deleted task to the workspace trash, where it can still be restored. A rehearsal mode locates the task and reports what would be deleted without removing it.

### How do I automatically delete a task from a ClickUp list on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/delete_task, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/delete_task

### Is there a app.clickup.com API to delete a task from a ClickUp list?

You do not need one. "Delete a task from a ClickUp list" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: listId, taskId. Optional: dry_run, workspaceId.

### What does it return?

It returns dryRun, listId, taskId, deleted, listName, taskName, tasksAfter, accountUsed, tasksBefore, workspaceId, movedToTrash, verifiedGone, outcomeConfirmed.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It makes changes on app.clickup.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/delete_task, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/delete_task

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/delete_task
