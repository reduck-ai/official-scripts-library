# List the tasks in a ClickUp list

Automatically list the tasks in a ClickUp list on app.clickup.com. Reads the tasks shown in one ClickUp list, in the order the list displays them, returning each task's identifier, name, status, assignees and link. Pair it with the ClickUp list lookup to go from a list name to its identifier.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/list_tasks`
- Updated: 2026-09-23 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/list_tasks`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/list_tasks
```

## Input

- `listId` (string, required): Numeric ClickUp list id, as returned by the ClickUp list lookup.
- `workspaceId` (string, optional): Numeric ClickUp workspace id. Supplying it skips a lookup step and is faster; omit it to let ClickUp resolve the default workspace first.

## Output

- `tasks` (array, required)
- `listId` (string, required)
- `listName` (string | null, required)
- `taskCount` (integer, required)
- `workspaceId` (string, required)
- `renderedRowCount` (integer, required)
- `listArchived` (boolean | null, optional)
- `hydratedForEveryRow` (boolean, optional)

## FAQ

### What does "List the tasks in a ClickUp list" do?

Reads the tasks shown in one ClickUp list, in the order the list displays them, returning each task's identifier, name, status, assignees and link. Pair it with the ClickUp list lookup to go from a list name to its identifier.

### How do I automatically list the tasks in a ClickUp list on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/list_tasks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/list_tasks

### Is there a app.clickup.com API to list the tasks in a ClickUp list?

You do not need one. "List the tasks in a ClickUp list" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: listId. Optional: workspaceId.

### What does it return?

It returns tasks, listId, listName, taskCount, workspaceId, listArchived, renderedRowCount, hydratedForEveryRow.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It only reads. It looks things up on app.clickup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/list_tasks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/list_tasks

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/list_tasks
