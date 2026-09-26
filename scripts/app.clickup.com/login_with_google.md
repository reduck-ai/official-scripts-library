# ClickUp login (Google SSO)

Log into ClickUp with Continue with Google, picking the given Google account, and land in your ClickUp workspace. Returns straight away if already signed in, and reports the ClickUp account that is signed in. Needs a browser that is already signed in to that Google account.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/login_with_google`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/login_with_google
```

## Input

- `email` (string, required): The Google account (email) to sign in to ClickUp with.

## Output

- `already` (boolean, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `account` (string | null, optional)

## FAQ

### What does "ClickUp login (Google SSO)" do?

Log into ClickUp with Continue with Google, picking the given Google account, and land in your ClickUp workspace. Returns straight away if already signed in, and reports the ClickUp account that is signed in. Needs a browser that is already signed in to that Google account.

### What information do I need to provide?

Required: email.

### What does it return?

It returns name, account, already, loggedIn.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It makes changes on app.clickup.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/login_with_google
