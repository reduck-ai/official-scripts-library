# Get current Lovable user

Automatically get current Lovable user on lovable.dev. Report which Lovable account this browser is signed in as: user id, email, display name, photo and whether the email is verified, from the app's own account lookup. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Lovable scripts.

- Site: lovable.dev
- Address: `reduck/lovable.dev/get_current_user`
- Updated: 2026-09-28 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lovable.dev/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lovable.dev/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `email` (string | null, optional)
- `photoUrl` (string | null, optional)
- `displayName` (string | null, optional)
- `emailVerified` (boolean | null, optional)

## FAQ

### What does "Get current Lovable user" do?

Report which Lovable account this browser is signed in as: user id, email, display name, photo and whether the email is verified, from the app's own account lookup. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Lovable scripts.

### How do I automatically get current Lovable user on lovable.dev?

Ask an AI agent connected to Reduck to run reduck/lovable.dev/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lovable.dev/get_current_user

### Is there a lovable.dev API to get current Lovable user?

You do not need one. "Get current Lovable user" drives the real lovable.dev pages in a browser, so it works whether or not lovable.dev offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, email, loggedIn, photoUrl, displayName, emailVerified.

### Do I need to be logged in to lovable.dev?

Yes. It acts as you on lovable.dev: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the lovable.dev cookies saved by the Reduck extension.

### Does it change anything on lovable.dev, or only read data?

It only reads. It looks things up on lovable.dev and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lovable.dev/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lovable.dev/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lovable.dev/get_current_user
