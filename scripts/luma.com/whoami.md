# Luma whoami (signed-in account)

Report which Luma account this browser is signed in as: the account email, the Luma user id, the username and the display name. If the browser is not signed in to Luma, the run fails with a signed-out error that says to sign in, then retry.

- Site: luma.com
- Address: `reduck/luma.com/whoami`
- Updated: 2026-11-18 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/whoami
```

## Input

It takes no input.

## Output

- `name` (string | null, required): The account's display name.
- `userId` (string | null, required): Luma user id, e.g. usr-XXXXXXXXXXXXXXX.
- `account` (string | null, required): The signed-in account's email. Null when Luma shows no email.
- `loggedIn` (boolean, required): Whether this browser is signed in to Luma (whoami format). Signed out throws SignedOutError.
- `username` (string | null, required): Luma username (luma.com/user/<username>). Null when the account never picked one.
- `connected` (boolean, required): Kept for older callers; same value as loggedIn.

## FAQ

### What does "Luma whoami (signed-in account)" do?

Report which Luma account this browser is signed in as: the account email, the Luma user id, the username and the display name. If the browser is not signed in to Luma, the run fails with a signed-out error that says to sign in, then retry.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, userId, account, loggedIn, username, connected.

### Do I need to be logged in to luma.com?

Yes. It acts as you on luma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the luma.com cookies saved by the Reduck extension.

### Does it change anything on luma.com, or only read data?

It only reads. It looks things up on luma.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/whoami
