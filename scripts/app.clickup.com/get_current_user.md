# Get current ClickUp user

Automatically get current ClickUp user on app.clickup.com. Report which ClickUp account this browser is signed in as: the full name and email. The name is null when the account has none. When the browser is signed out of ClickUp, the run fails with a signed-out error asking you to sign in to app.clickup.com.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/get_current_user`
- Updated: 2026-10-22 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/get_current_user
```

## Input

It takes no input.

## Output

- `email` (string, required)
- `name` (string | null, optional)

## FAQ

### What does "Get current ClickUp user" do?

Report which ClickUp account this browser is signed in as: the full name and email. The name is null when the account has none. When the browser is signed out of ClickUp, the run fails with a signed-out error asking you to sign in to app.clickup.com.

### How do I automatically get current ClickUp user on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/get_current_user

### Is there a app.clickup.com API to get current ClickUp user?

You do not need one. "Get current ClickUp user" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It only reads. It looks things up on app.clickup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/get_current_user
