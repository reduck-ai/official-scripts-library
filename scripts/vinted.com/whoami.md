# Vinted whoami

Report which Vinted account this browser is signed in as on a country site (vinted.fr by default; pass `domain`, e.g. www.vinted.com): the account email from account settings. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Vinted scripts.

- Site: vinted.com
- Address: `reduck/vinted.com/whoami`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vinted.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vinted.com/whoami
```

## Input

- `domain` (string, optional): Vinted country site, e.g. "www.vinted.fr" (default) or "www.vinted.com". Vinted accounts are per country site.

## Output

- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `domain` (string, optional)

## FAQ

### What does "Vinted whoami" do?

Report which Vinted account this browser is signed in as on a country site (vinted.fr by default; pass `domain`, e.g. www.vinted.com): the account email from account settings. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Vinted scripts.

### What information do I need to provide?

Optional: domain.

### What does it return?

It returns email, domain, loggedIn.

### Do I need to be logged in to vinted.com?

Yes. It acts as you on vinted.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vinted.com cookies saved by the Reduck extension.

### Does it change anything on vinted.com, or only read data?

It only reads. It looks things up on vinted.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vinted.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vinted.com/whoami
