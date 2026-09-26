# TikTok login (Google SSO)

Log into TikTok with Continue with Google, picking the given Google account in Google's sign-in window. Returns straight away if already signed in, and reports the TikTok @username that is signed in. Needs a browser that is already signed in to that Google account, and the Google account must already be linked to a TikTok account.

- Site: tiktok.com
- Address: `reduck/tiktok.com/login_with_google`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/login_with_google
```

## Input

- `email` (string, required): The Google account (email) linked to the TikTok account to sign in with.

## Output

- `already` (boolean, required)
- `loggedIn` (boolean, required)
- `userId` (string | null, optional)
- `nickname` (string | null, optional)
- `username` (string | null, optional)

## FAQ

### What does "TikTok login (Google SSO)" do?

Log into TikTok with Continue with Google, picking the given Google account in Google's sign-in window. Returns straight away if already signed in, and reports the TikTok @username that is signed in. Needs a browser that is already signed in to that Google account, and the Google account must already be linked to a TikTok account.

### What information do I need to provide?

Required: email.

### What does it return?

It returns userId, already, loggedIn, nickname, username.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/login_with_google
