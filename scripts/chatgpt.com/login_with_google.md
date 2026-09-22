# OpenAI (ChatGPT) login (Google SSO)

Log into OpenAI / ChatGPT via Google SSO — picks the right account when several are signed in, and does nothing if you're already logged in. If Google interrupts the flow with a password re-confirmation or a 2FA step-up, the script can't complete that step on its own; sign in once manually in the same browser to clear the step-up, then re-run. It may also occasionally fail to complete a fresh login due to the site's own anti-automation checks — if that happens, try again shortly.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/login_with_google`
- Updated: 2026-08-21 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser when several are signed in. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)
- `already` (boolean, optional): true if a session already existed (no Google click needed)

## FAQ

### What does "OpenAI (ChatGPT) login (Google SSO)" do?

Log into OpenAI / ChatGPT via Google SSO — picks the right account when several are signed in, and does nothing if you're already logged in. If Google interrupts the flow with a password re-confirmation or a 2FA step-up, the script can't complete that step on its own; sign in once manually in the same browser to clear the step-up, then re-run. It may also occasionally fail to complete a fresh login due to the site's own anti-automation checks — if that happens, try again shortly.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to chatgpt.com?

Yes. It acts as you on chatgpt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chatgpt.com cookies saved by the Reduck extension.

### Does it change anything on chatgpt.com, or only read data?

It makes changes on chatgpt.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/login_with_google
