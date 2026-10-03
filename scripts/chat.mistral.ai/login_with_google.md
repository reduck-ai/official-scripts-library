# Le Chat (Mistral) login (Google SSO)

Log into Le Chat (chat.mistral.ai) with Google sign-in, handling the Google account chooser and consent screen. Returns straight away if this browser is already signed in, and reports the Mistral account email. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that already has a Mistral account.

- Site: chat.mistral.ai
- Address: `reduck/chat.mistral.ai/login_with_google`
- Updated: 2026-10-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chat.mistral.ai/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): Mistral account email

## FAQ

### What does "Le Chat (Mistral) login (Google SSO)" do?

Log into Le Chat (chat.mistral.ai) with Google sign-in, handling the Google account chooser and consent screen. Returns straight away if this browser is already signed in, and reports the Mistral account email. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that already has a Mistral account.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to chat.mistral.ai?

No. It only uses pages of chat.mistral.ai that are reachable without signing in.

### Does it change anything on chat.mistral.ai, or only read data?

It makes changes on chat.mistral.ai, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chat.mistral.ai/login_with_google
