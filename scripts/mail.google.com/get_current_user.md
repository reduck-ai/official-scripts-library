# Get Current Gmail User

Automatically get Current Gmail User on mail.google.com. Return the display name and email of the Gmail account this browser is signed in as.

- Site: mail.google.com
- Address: `reduck/mail.google.com/get_current_user`
- Updated: 2026-10-05 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/get_current_user
```

## Input

It takes no input.

## Output

- `name` (string, required)
- `email` (string, required)

## FAQ

### What does "Get Current Gmail User" do?

Return the display name and email of the Gmail account this browser is signed in as.

### How do I automatically get Current Gmail User on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/get_current_user

### Is there a mail.google.com API to get Current Gmail User?

You do not need one. "Get Current Gmail User" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/get_current_user
