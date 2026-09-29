# Get Current Notion User

Automatically get Current Notion User on app.notion.com. Report which Notion account this browser is signed in as: email, name, the current workspace and every workspace the account belongs to. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Notion scripts.

- Site: app.notion.com
- Address: `reduck/app.notion.com/get_current_user`
- Updated: 2026-09-28 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `workspaces` (array, optional)
- `workspaceName` (string | null, optional)

## FAQ

### What does "Get Current Notion User" do?

Report which Notion account this browser is signed in as: email, name, the current workspace and every workspace the account belongs to. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Notion scripts.

### How do I automatically get Current Notion User on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/get_current_user

### Is there a app.notion.com API to get Current Notion User?

You do not need one. "Get Current Notion User" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn, workspaces, workspaceName.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/get_current_user
