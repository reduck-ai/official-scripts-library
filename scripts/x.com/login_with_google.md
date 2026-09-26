# X (Twitter) login (Google SSO)

Log into X (Twitter) with Continue with Google, picking the given Google account in Google's sign-in window, and land on the X home timeline. Returns straight away if already signed in, and reports the X handle that is signed in. Needs a browser that is already signed in to that Google account.

- Site: x.com
- Address: `reduck/x.com/login_with_google`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/login_with_google
```

## Input

- `email` (string, required): The Google account (email) linked to the X account to sign in with. Picking an account that has no X account opens X's sign-up flow instead.

## Output

- `already` (boolean, required)
- `loggedIn` (boolean, required)
- `stage` (string | null, optional)
- `handle` (string | null, optional)
- `userId` (string | null, optional)

## FAQ

### What does "X (Twitter) login (Google SSO)" do?

Log into X (Twitter) with Continue with Google, picking the given Google account in Google's sign-in window, and land on the X home timeline. Returns straight away if already signed in, and reports the X handle that is signed in. Needs a browser that is already signed in to that Google account.

### What information do I need to provide?

Required: email.

### What does it return?

It returns stage, handle, userId, already, loggedIn.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/login_with_google
