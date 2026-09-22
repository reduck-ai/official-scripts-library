# List Slack drafts

Automatically list Slack drafts on slack.com. List your unsent message drafts. Returns each draft's id, destination channel(s) and text. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_drafts`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_drafts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_drafts
```

## Input

- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `drafts` (array, required)

## FAQ

### What does "List Slack drafts" do?

List your unsent message drafts. Returns each draft's id, destination channel(s) and text. Requires login.

### How do I automatically list Slack drafts on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_drafts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_drafts

### Is there a slack.com API to list Slack drafts?

You do not need one. "List Slack drafts" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: workspaceDomain.

### What does it return?

It returns drafts.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_drafts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_drafts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_drafts
