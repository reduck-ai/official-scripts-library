# Get Slack user profile

Automatically get Slack user profile on slack.com. Get one member's full profile by id (U…) or by handle/display name (resolved via the member directory). Returns handle, real/display name, title, email (when visible), timezone, status and admin/owner/bot/guest flags. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_user_profile`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_user_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_user_profile
```

## Input

- `user` (string, required): Member id (U…) or handle/display name (e.g. 'tester.account').
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `id` (string, required)
- `tz` (string | null, optional)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `image` (string | null, optional)
- `phone` (string | null, optional)
- `title` (string | null, optional)
- `is_bot` (boolean, optional)
- `deleted` (boolean, optional)
- `is_admin` (boolean, optional)
- `is_owner` (boolean, optional)
- `tz_label` (string | null, optional)
- `real_name` (string | null, optional)
- `status_text` (string | null, optional)
- `display_name` (string | null, optional)
- `status_emoji` (string | null, optional)
- `is_restricted` (boolean, optional)
- `is_ultra_restricted` (boolean, optional)

## FAQ

### What does "Get Slack user profile" do?

Get one member's full profile by id (U…) or by handle/display name (resolved via the member directory). Returns handle, real/display name, title, email (when visible), timezone, status and admin/owner/bot/guest flags. Requires login.

### How do I automatically get Slack user profile on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_user_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_user_profile

### Is there a slack.com API to get Slack user profile?

You do not need one. "Get Slack user profile" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: user. Optional: workspaceDomain.

### What does it return?

It returns id, tz, name, email, image, phone, title, is_bot, deleted, is_admin, is_owner, tz_label, real_name, status_text, display_name, status_emoji, is_restricted, is_ultra_restricted.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_user_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_user_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_user_profile
