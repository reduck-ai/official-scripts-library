# List Google accounts signed in on this browser (Gmail)

Automatically list Google accounts signed in on this browser (Gmail) on mail.google.com. List the Google accounts signed in on this browser, as the Gmail account switcher shows them. Each account comes back with its address, the index that addresses it in a Google URL, and whether it is the one Gmail opens by default. The index is what the other Gmail scripts take as their account argument, so this answers which account a script acts as when none is given.

- Site: mail.google.com
- Address: `reduck/mail.google.com/list_accounts`
- Updated: 2026-09-22 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/list_accounts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_accounts
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `accounts` (array, required): Signed-in accounts, ordered by index.

## FAQ

### What does "List Google accounts signed in on this browser (Gmail)" do?

List the Google accounts signed in on this browser, as the Gmail account switcher shows them. Each account comes back with its address, the index that addresses it in a Google URL, and whether it is the one Gmail opens by default. The index is what the other Gmail scripts take as their account argument, so this answers which account a script acts as when none is given.

### How do I automatically list Google accounts signed in on this browser (Gmail) on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/list_accounts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_accounts

### Is there a mail.google.com API to list Google accounts signed in on this browser (Gmail)?

You do not need one. "List Google accounts signed in on this browser (Gmail)" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, accounts.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/list_accounts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_accounts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/list_accounts
