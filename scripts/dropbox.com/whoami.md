# Dropbox whoami (signed-in account)

Report which Dropbox account this browser is signed in as: the account id, numeric user id, email, display name, account type (basic, plus, business…) and country. When the browser is not signed in to Dropbox, the run fails with a signed-out error that says to sign in, then retry. It only reads and never signs an account in.

- Site: dropbox.com
- Address: `reduck/dropbox.com/whoami`
- Updated: 2026-10-20 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dropbox.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dropbox.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `country` (string | null, optional)
- `accountId` (string | null, optional)
- `accountType` (string | null, optional)

## FAQ

### What does "Dropbox whoami (signed-in account)" do?

Report which Dropbox account this browser is signed in as: the account id, numeric user id, email, display name, account type (basic, plus, business…) and country. When the browser is not signed in to Dropbox, the run fails with a signed-out error that says to sign in, then retry. It only reads and never signs an account in.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, userId, country, evidence, loggedIn, accountId, accountType.

### Do I need to be logged in to dropbox.com?

Yes. It acts as you on dropbox.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dropbox.com cookies saved by the Reduck extension.

### Does it change anything on dropbox.com, or only read data?

It only reads. It looks things up on dropbox.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dropbox.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropbox.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dropbox.com/whoami
