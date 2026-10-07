# Get Current User

Automatically get Current User on app.pennylane.com. Report which Pennylane account this browser is signed in as: email and name from the app's own users/me. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Pennylane scripts.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/get_current_user`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Get Current User" do?

Report which Pennylane account this browser is signed in as: email and name from the app's own users/me. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Pennylane scripts.

### How do I automatically get Current User on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/get_current_user

### Is there a app.pennylane.com API to get Current User?

You do not need one. "Get Current User" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It only reads. It looks things up on app.pennylane.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/get_current_user
