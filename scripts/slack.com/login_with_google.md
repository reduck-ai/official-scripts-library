# Slack login (Google SSO)

Log into a Slack workspace using Sign in with Google, then open that workspace. Handles Google's account chooser and consent along the way. Pass the workspace subdomain (e.g. "myteam" for myteam.slack.com) and optionally which Google account to use; your Google account must already have access to the workspace.

- Site: slack.com
- Address: `reduck/slack.com/login_with_google`
- Updated: 2026-08-21 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/login_with_google
```

## Input

- `workspace` (string, required): Slack workspace subdomain to open, e.g. "myteam" for myteam.slack.com. Must be one your Google account can access.
- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `workspace` (string, required)
- `account` (string | null, optional)

## FAQ

### What does "Slack login (Google SSO)" do?

Log into a Slack workspace using Sign in with Google, then open that workspace. Handles Google's account chooser and consent along the way. Pass the workspace subdomain (e.g. "myteam" for myteam.slack.com) and optionally which Google account to use; your Google account must already have access to the workspace.

### What information do I need to provide?

Required: workspace. Optional: email.

### What does it return?

It returns url, account, loggedIn, workspace.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/login_with_google
