# Get current Product Hunt user

Automatically get current Product Hunt user on producthunt.com. Report which Product Hunt account this browser is signed in as: the @username, display name, numeric user id and profile URL. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Product Hunt scripts.

- Site: producthunt.com
- Address: `reduck/producthunt.com/get_current_user`
- Updated: 2026-09-30 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `userId` (string | null, optional)
- `username` (string | null, optional): Product Hunt handle, without the @
- `profileUrl` (string | null, optional)

## FAQ

### What does "Get current Product Hunt user" do?

Report which Product Hunt account this browser is signed in as: the @username, display name, numeric user id and profile URL. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Product Hunt scripts.

### How do I automatically get current Product Hunt user on producthunt.com?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_current_user

### Is there a producthunt.com API to get current Product Hunt user?

You do not need one. "Get current Product Hunt user" drives the real producthunt.com pages in a browser, so it works whether or not producthunt.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, userId, loggedIn, username, profileUrl.

### Do I need to be logged in to producthunt.com?

Yes. It acts as you on producthunt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the producthunt.com cookies saved by the Reduck extension.

### Does it change anything on producthunt.com, or only read data?

It only reads. It looks things up on producthunt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/get_current_user
