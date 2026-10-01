# Linear whoami (signed-in account)

Report which Linear account this browser is signed in as: name, email and the workspace slug, from Personal Profile settings. Optionally pass `workspaceUrl` to read a specific workspace. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Linear scripts.

- Site: linear.app
- Address: `reduck/linear.app/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linear.app/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linear.app/whoami
```

## Input

- `workspaceUrl` (string, optional): Workspace slug (from its Linear URL). Defaults to whatever workspace the account lands on.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `workspace` (string | null, optional): Workspace slug the profile page opened in

## FAQ

### What does "Linear whoami (signed-in account)" do?

Report which Linear account this browser is signed in as: name, email and the workspace slug, from Personal Profile settings. Optionally pass `workspaceUrl` to read a specific workspace. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Linear scripts.

### What information do I need to provide?

Optional: workspaceUrl.

### What does it return?

It returns name, email, loggedIn, workspace.

### Do I need to be logged in to linear.app?

Yes. It acts as you on linear.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linear.app cookies saved by the Reduck extension.

### Does it change anything on linear.app, or only read data?

It only reads. It looks things up on linear.app and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linear.app/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linear.app/whoami
