# List my assigned ClickUp tasks

Automatically list my assigned ClickUp tasks on app.clickup.com. Returns the tasks assigned to the signed-in person, as ClickUp's Home page shows them, with each task's status, priority, due date and the list it belongs to. Reports how the answer was confirmed, so an empty result is never mistaken for a page that had not finished loading.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/list_my_tasks`
- Updated: 2026-09-23 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/list_my_tasks`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/list_my_tasks
```

## Input

- `workspaceId` (string, optional): Numeric ClickUp workspace id. Supplying it skips a lookup step; omit it to let ClickUp resolve the default workspace.

## Output

- `tasks` (array, required)
- `taskCount` (number, required)
- `confirmedBy` (string, required): task-details means the tasks came from ClickUp's own answer and the page agreed with it. empty-card means the card was there with nothing in it, which is the weaker evidence of the two.
- `workspaceId` (string, required)
- `url` (string, optional)
- `accountUsed` (string | null, optional)
- `renderedCount` (number, optional)

## FAQ

### What does "List my assigned ClickUp tasks" do?

Returns the tasks assigned to the signed-in person, as ClickUp's Home page shows them, with each task's status, priority, due date and the list it belongs to. Reports how the answer was confirmed, so an empty result is never mistaken for a page that had not finished loading.

### How do I automatically list my assigned ClickUp tasks on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/list_my_tasks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/list_my_tasks

### Is there a app.clickup.com API to list my assigned ClickUp tasks?

You do not need one. "List my assigned ClickUp tasks" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Optional: workspaceId.

### What does it return?

It returns url, tasks, taskCount, accountUsed, confirmedBy, workspaceId, renderedCount.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It only reads. It looks things up on app.clickup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/list_my_tasks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/list_my_tasks

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/list_my_tasks
