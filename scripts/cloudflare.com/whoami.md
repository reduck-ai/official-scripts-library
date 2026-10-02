# Cloudflare whoami (signed-in account)

Report which Cloudflare account this browser is signed in as: email, display name (first + last name from the profile; null when none is set) and user id, from the dashboard's own user API. Being signed out is a normal answer (loggedIn false), not an error.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/whoami`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `email` (string | null, optional)
- `displayName` (string | null, optional)

## FAQ

### What does "Cloudflare whoami (signed-in account)" do?

Report which Cloudflare account this browser is signed in as: email, display name (first + last name from the profile; null when none is set) and user id, from the dashboard's own user API. Being signed out is a normal answer (loggedIn false), not an error.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, email, loggedIn, displayName.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

It only reads. It looks things up on cloudflare.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/whoami
