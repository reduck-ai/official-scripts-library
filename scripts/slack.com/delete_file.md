# Delete Slack file

Automatically delete Slack file on slack.com. Delete a file you own by its id (F…). Permanent. Returns the deleted file id. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/delete_file`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/delete_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/delete_file
```

## Input

- `file` (string, required): File id (F…) to delete.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `file` (string, required)

## FAQ

### What does "Delete Slack file" do?

Delete a file you own by its id (F…). Permanent. Returns the deleted file id. Requires login.

### How do I automatically delete Slack file on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/delete_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/delete_file

### Is there a slack.com API to delete Slack file?

You do not need one. "Delete Slack file" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: file. Optional: workspaceDomain.

### What does it return?

It returns ok, file.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/delete_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/delete_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/delete_file
