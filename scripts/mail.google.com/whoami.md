# Gmail whoami (signed-in account)

Report which Gmail account this browser is signed in as: display name and email, from Gmail's account switcher. When the browser is signed out, the run fails with a signed-out error that asks to sign in to Gmail, so it can be used to check a session before running other Gmail scripts.

- Site: mail.google.com
- Address: `reduck/mail.google.com/whoami`
- Updated: 2026-10-22 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/whoami
```

## Input

- `account` (string, optional): Optional Google account to report on, for a browser signed into several: its email address, or a bare mailbox index such as "2". Omit for the first account (u/0).

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Gmail whoami (signed-in account)" do?

Report which Gmail account this browser is signed in as: display name and email, from Gmail's account switcher. When the browser is signed out, the run fails with a signed-out error that asks to sign in to Gmail, so it can be used to check a session before running other Gmail scripts.

### What information do I need to provide?

Optional: account.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/whoami
