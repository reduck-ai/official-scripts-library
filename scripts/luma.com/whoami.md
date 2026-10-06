# Luma whoami (signed-in account)

Report which Luma account this browser is signed in as: the account email, the Luma user id, the username and the display name. Being signed out is a normal answer (connected false), not an error, so it can check a session before other Luma scripts run, or be passed as a run's login probe.

- Site: luma.com
- Address: `reduck/luma.com/whoami`
- Updated: 2026-10-05 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/whoami
```

## Input

It takes no input.

## Output

- `name` (string | null, required): The account's display name. Null when signed out.
- `userId` (string | null, required): Luma user id, e.g. usr-XXXXXXXXXXXXXXX. It stays the same if the account's email changes. Null when signed out.
- `account` (string | null, required): The signed-in account's email, which a login probe records on the connector it checked. Null when signed out, or when Luma shows no email.
- `username` (string | null, required): Luma username (luma.com/user/<username>). Null when signed out, or when the account never picked one.
- `connected` (boolean, required): Whether this browser is signed in to Luma. Signed out is false, not an error, so the script can be passed as a run's `login.probe`.

## FAQ

### What does "Luma whoami (signed-in account)" do?

Report which Luma account this browser is signed in as: the account email, the Luma user id, the username and the display name. Being signed out is a normal answer (connected false), not an error, so it can check a session before other Luma scripts run, or be passed as a run's login probe.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, userId, account, username, connected.

### Do I need to be logged in to luma.com?

Yes. It acts as you on luma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the luma.com cookies saved by the Reduck extension.

### Does it change anything on luma.com, or only read data?

It only reads. It looks things up on luma.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/whoami
