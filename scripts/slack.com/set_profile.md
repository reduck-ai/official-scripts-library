# Set Slack profile

Automatically set Slack profile on slack.com. Update your own profile: display name, real name and/or phone. Only the fields you pass change; the update is read back and confirmed. Title and pronouns are governed by workspace policy and often not settable via the web session, so they are not exposed here. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/set_profile`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/set_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/set_profile
```

## Input

- `phone` (string, optional): Phone number.
- `realName` (string, optional): Full/real name.
- `displayName` (string, optional): Display name (@-name shown to others).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `phone` (string | null, optional)
- `realName` (string | null, optional)
- `displayName` (string | null, optional)

## FAQ

### What does "Set Slack profile" do?

Update your own profile: display name, real name and/or phone. Only the fields you pass change; the update is read back and confirmed. Title and pronouns are governed by workspace policy and often not settable via the web session, so they are not exposed here. Requires login.

### How do I automatically set Slack profile on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_profile

### Is there a slack.com API to set Slack profile?

You do not need one. "Set Slack profile" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: phone, realName, displayName, workspaceDomain.

### What does it return?

It returns ok, phone, realName, displayName.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/set_profile
