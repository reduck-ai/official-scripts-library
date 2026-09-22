# Create Slack channel

Automatically create Slack channel on slack.com. Create a new channel. The name is normalized to Slack's rules (lowercased, spaces/invalid chars → hyphens, max 80 chars) so 'test 123' becomes 'test-123'. Pass isPrivate for a private channel. Returns the new channel's id and (normalized) name. Requires login (and permission to create channels).

- Site: slack.com
- Address: `reduck/slack.com/create_channel`
- Updated: 2026-07-31 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/create_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/create_channel
```

## Input

- `name` (string, required): Channel name (lowercase, hyphens; Slack normalizes it).
- `isPrivate` (boolean, optional): Create a private channel. Default false.
- `workspaceDomain` (string, optional): Workspace host. Defaults to the active workspace.

## Output

- `id` (string, required)
- `ok` (boolean, required)
- `name` (string, required)
- `is_private` (boolean, optional)

## FAQ

### What does "Create Slack channel" do?

Create a new channel. The name is normalized to Slack's rules (lowercased, spaces/invalid chars → hyphens, max 80 chars) so 'test 123' becomes 'test-123'. Pass isPrivate for a private channel. Returns the new channel's id and (normalized) name. Requires login (and permission to create channels).

### How do I automatically create Slack channel on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/create_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/create_channel

### Is there a slack.com API to create Slack channel?

You do not need one. "Create Slack channel" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: isPrivate, workspaceDomain.

### What does it return?

It returns id, ok, name, is_private.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/create_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/create_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/create_channel
