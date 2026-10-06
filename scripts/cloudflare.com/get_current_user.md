# Get current user

Automatically get current user on cloudflare.com. Report which Cloudflare account this browser is signed in as: email, display name (first + last name from the profile; null when none is set) and user id, from the dashboard's own user API. Being signed out is a normal answer (loggedIn false), not an error.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/get_current_user`
- Updated: 2026-10-05 (v3)
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
- `email` (string | null, optional)
- `displayName` (string | null, optional)

## FAQ

### What does "Get current user" do?

Report which Cloudflare account this browser is signed in as: email, display name (first + last name from the profile; null when none is set) and user id, from the dashboard's own user API. Being signed out is a normal answer (loggedIn false), not an error.

### How do I automatically get current user on cloudflare.com?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/get_current_user

### Is there a cloudflare.com API to get current user?

You do not need one. "Get current user" drives the real cloudflare.com pages in a browser, so it works whether or not cloudflare.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, email, loggedIn, displayName.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

It only reads. It looks things up on cloudflare.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/get_current_user
