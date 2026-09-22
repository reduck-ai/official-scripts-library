# Create Slack draft

Automatically create Slack draft on slack.com. Write an unsent draft message to a channel or DM (by name '#social', channel/DM id C…/D…, or @handle/U… for a DM). The draft appears in your Drafts and in list_drafts; it is not sent. Slack allows only one draft per conversation: if one already exists for the destination the call errors (delete/send it first). Returns the new draft id. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/create_draft`
- Updated: 2026-07-31 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/create_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/create_draft
```

## Input

- `text` (string, required): Draft body text.
- `channel` (string, required): Destination: channel name/#name, id (C…/D…), or @handle/U… for a DM.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `id` (string | null, required)
- `ok` (boolean, required)
- `channel` (string, optional)
- `dateCreated` (integer | null, optional)

## FAQ

### What does "Create Slack draft" do?

Write an unsent draft message to a channel or DM (by name '#social', channel/DM id C…/D…, or @handle/U… for a DM). The draft appears in your Drafts and in list_drafts; it is not sent. Slack allows only one draft per conversation: if one already exists for the destination the call errors (delete/send it first). Returns the new draft id. Requires login.

### How do I automatically create Slack draft on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/create_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/create_draft

### Is there a slack.com API to create Slack draft?

You do not need one. "Create Slack draft" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, text. Optional: workspaceDomain.

### What does it return?

It returns id, ok, channel, dateCreated.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/create_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/create_draft

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/create_draft
