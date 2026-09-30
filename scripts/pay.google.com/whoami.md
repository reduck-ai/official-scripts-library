# Google Pay whoami

Report which Google account this browser uses on Google Pay (email and name) and whether it has a Google Pay payments profile — without one, Google Pay sends the account to its sign-up page and Google Pay scripts have nothing to read. Being signed out of Google is reported as a normal answer (loggedIn false), not an error.

- Site: pay.google.com
- Address: `reduck/pay.google.com/whoami`
- Updated: 2026-09-29 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pay.google.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pay.google.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `hasPaymentsProfile` (boolean | null, optional): false when Google Pay sends the account to its sign-up page (no payments profile yet), so Google Pay scripts cannot read anything

## FAQ

### What does "Google Pay whoami" do?

Report which Google account this browser uses on Google Pay (email and name) and whether it has a Google Pay payments profile — without one, Google Pay sends the account to its sign-up page and Google Pay scripts have nothing to read. Being signed out of Google is reported as a normal answer (loggedIn false), not an error.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn, hasPaymentsProfile.

### Do I need to be logged in to pay.google.com?

Yes. It acts as you on pay.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the pay.google.com cookies saved by the Reduck extension.

### Does it change anything on pay.google.com, or only read data?

It only reads. It looks things up on pay.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pay.google.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pay.google.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pay.google.com/whoami
