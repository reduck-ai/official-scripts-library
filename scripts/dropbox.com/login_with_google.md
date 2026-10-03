# Dropbox login

Log into Dropbox via Google SSO. Drives Dropbox's Continue-with-Google flow, picks the account (optional email arg), clears consent, and lands on the Dropbox home. Requires an active Google session in the browser; not available on cloud/managed browsers.

- Site: dropbox.com
- Address: `reduck/dropbox.com/login_with_google`
- Updated: 2026-10-02 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dropbox.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dropbox.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): The signed-in Dropbox account, read back from Dropbox's own account menu. Null only when no address could be read — never an unverified echo of the `email` argument.

## FAQ

### What does "Dropbox login" do?

Log into Dropbox via Google SSO. Drives Dropbox's Continue-with-Google flow, picks the account (optional email arg), clears consent, and lands on the Dropbox home. Requires an active Google session in the browser; not available on cloud/managed browsers.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to dropbox.com?

Yes. It acts as you on dropbox.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dropbox.com cookies saved by the Reduck extension.

### Does it change anything on dropbox.com, or only read data?

It makes changes on dropbox.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dropbox.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropbox.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dropbox.com/login_with_google
