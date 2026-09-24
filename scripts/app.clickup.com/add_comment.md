# Add a comment to a ClickUp task

Automatically add a comment to a ClickUp task on app.clickup.com. Posts a comment on a ClickUp task and confirms it appears, returning the new comment's identifier. It reports whether the same text is already on the task, so a repeat does not quietly duplicate it. A rehearsal mode fills the comment box and stops before sending.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/add_comment`
- Updated: 2026-09-23 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/add_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/add_comment
```

## Input

- `taskId` (string, required): The task's ClickUp id, as returned by the ClickUp task listing or by task creation.
- `comment` (string, required): The comment text. Plain text; line breaks become separate paragraphs. Written as pasted text, so a leading slash stays literal instead of opening ClickUp's command menu.
- `dry_run` (boolean, optional): Rehearse without posting. The comment box is filled in and checked that it is ready to send, then the run stops on the step before the one that sends it.
- `workspaceId` (string, optional): Numeric ClickUp workspace id. Supplying it skips a lookup step; omit it to let ClickUp resolve the default workspace.

## Output

- `dryRun` (boolean, required)
- `posted` (boolean, required)
- `taskId` (string, required)
- `workspaceId` (string, required)
- `url` (string, optional)
- `taskName` (string | null, optional)
- `commentId` (string | null, optional)
- `accountUsed` (string | null, optional)
- `composerReady` (boolean, optional)
- `alreadyPresent` (boolean | null, optional): Whether the same text was already on the task before this run. Null when ClickUp did not return the task's activity, so the answer is unknown rather than no.
- `verifiedOnPage` (boolean, optional)
- `outcomeConfirmed` (boolean, optional)

## FAQ

### What does "Add a comment to a ClickUp task" do?

Posts a comment on a ClickUp task and confirms it appears, returning the new comment's identifier. It reports whether the same text is already on the task, so a repeat does not quietly duplicate it. A rehearsal mode fills the comment box and stops before sending.

### How do I automatically add a comment to a ClickUp task on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/add_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/add_comment

### Is there a app.clickup.com API to add a comment to a ClickUp task?

You do not need one. "Add a comment to a ClickUp task" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: taskId, comment. Optional: dry_run, workspaceId.

### What does it return?

It returns url, dryRun, posted, taskId, taskName, commentId, accountUsed, workspaceId, composerReady, alreadyPresent, verifiedOnPage, outcomeConfirmed.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It makes changes on app.clickup.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/add_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/add_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/add_comment
