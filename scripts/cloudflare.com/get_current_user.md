# Cloudflare whoami (signed-in account)

Report which Cloudflare account this browser is signed in as: the user id, email and name (first + last name from the profile; null when none is set). When the browser is signed out of Cloudflare, the run fails with a signed-out error asking you to sign in to dash.cloudflare.com.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/get_current_user`
- Updated: 2026-11-18 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `displayName` (string | null, optional)

## FAQ

### What does "Cloudflare whoami (signed-in account)" do?

Report which Cloudflare account this browser is signed in as: the user id, email and name (first + last name from the profile; null when none is set). When the browser is signed out of Cloudflare, the run fails with a signed-out error asking you to sign in to dash.cloudflare.com.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, email, userId, loggedIn, displayName.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

It only reads. It looks things up on cloudflare.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/get_current_user
