# List Slack workspaces signed in on this browser

Automatically list Slack workspaces signed in on this browser on slack.com. List the Slack workspaces this browser is signed in to, as Slack's workspace switcher holds them. Each workspace comes back with its name, its id, its domain (for example acme.slack.com), whether it is the one Slack opens by default, and whether this browser still holds a session for it. The domain is what the other Slack scripts take as workspaceDomain, so this answers which workspace a script acts on when none is given. Nothing is marked as read. Fails with a signed-out error when the browser is not signed in to Slack.

- Site: slack.com
- Address: `reduck/slack.com/list_workspaces`
- Updated: 2026-11-13 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_workspaces`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_workspaces
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `workspaces` (array, required): The workspaces in the order Slack lists them.

## FAQ

### What does "List Slack workspaces signed in on this browser" do?

List the Slack workspaces this browser is signed in to, as Slack's workspace switcher holds them. Each workspace comes back with its name, its id, its domain (for example acme.slack.com), whether it is the one Slack opens by default, and whether this browser still holds a session for it. The domain is what the other Slack scripts take as workspaceDomain, so this answers which workspace a script acts on when none is given. Nothing is marked as read. Fails with a signed-out error when the browser is not signed in to Slack.

### How do I automatically list Slack workspaces signed in on this browser on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_workspaces, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_workspaces

### Is there a slack.com API to list Slack workspaces signed in on this browser?

You do not need one. "List Slack workspaces signed in on this browser" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, workspaces.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_workspaces, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_workspaces

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_workspaces
