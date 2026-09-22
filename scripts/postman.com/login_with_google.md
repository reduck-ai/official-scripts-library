# Postman login (Google SSO)

Log into Postman using your connected Google account. Signs in via Google's account chooser and lands on your Postman workspace.

- Site: postman.com
- Address: `reduck/postman.com/login_with_google`
- Updated: 2026-08-20 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/postman.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/postman.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)
- `already` (boolean, optional)

## FAQ

### What does "Postman login (Google SSO)" do?

Log into Postman using your connected Google account. Signs in via Google's account chooser and lands on your Postman workspace.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to postman.com?

Yes. It acts as you on postman.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the postman.com cookies saved by the Reduck extension.

### Does it change anything on postman.com, or only read data?

It makes changes on postman.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/postman.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/postman.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/postman.com/login_with_google
