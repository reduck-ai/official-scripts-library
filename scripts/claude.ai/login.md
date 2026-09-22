# Login (self-authenticating via email magic link)

Authenticate to claude.ai by email magic link, with no cookie injection: requests the link, reads it from Gmail in the same browser, and lands signed in. Requires an active Google session for that inbox. Returns {authenticated, method: existing|magic_link, email, orgs}. Chain it before other claude.ai scripts, e.g. list_invoices.

- Site: claude.ai
- Address: `reduck/claude.ai/login`
- Updated: 2026-09-07 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/login`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/login
```

## Input

- `email` (string, required): Claude account email. Its Gmail inbox must be reachable (Google session active in this browser).

## Output

- `orgs` (array, required)
- `email` (string, required)
- `method` (string, required)
- `authenticated` (boolean, required)

## FAQ

### What does "Login (self-authenticating via email magic link)" do?

Authenticate to claude.ai by email magic link, with no cookie injection: requests the link, reads it from Gmail in the same browser, and lands signed in. Requires an active Google session for that inbox. Returns {authenticated, method: existing|magic_link, email, orgs}. Chain it before other claude.ai scripts, e.g. list_invoices.

### What information do I need to provide?

Required: email.

### What does it return?

It returns orgs, email, method, authenticated.

### Do I need to be logged in to claude.ai?

No. It only uses pages of claude.ai that are reachable without signing in.

### Does it change anything on claude.ai, or only read data?

It makes changes on claude.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/login, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/login

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/login
