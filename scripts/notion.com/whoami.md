# Notion whoami (signed-in account)

Report which Notion account this browser is signed in as: the user id, email and name, plus the workspaces it belongs to. When the browser is signed out of Notion, it stops with a sign-in error instead of returning an answer.

- Site: notion.com
- Address: `reduck/notion.com/whoami`
- Updated: 2026-10-20 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notion.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notion.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `workspaces` (array, optional)
- `currentWorkspace` (string | null, optional)

## FAQ

### What does "Notion whoami (signed-in account)" do?

Report which Notion account this browser is signed in as: the user id, email and name, plus the workspaces it belongs to. When the browser is signed out of Notion, it stops with a sign-in error instead of returning an answer.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, userId, evidence, loggedIn, workspaces, currentWorkspace.

### Do I need to be logged in to notion.com?

Yes. It acts as you on notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the notion.com cookies saved by the Reduck extension.

### Does it change anything on notion.com, or only read data?

It only reads. It looks things up on notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notion.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notion.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/notion.com/whoami
