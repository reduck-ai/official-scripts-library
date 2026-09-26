# Pipedrive login (Google SSO)

Log into Pipedrive with the Google button, handling the Google account chooser and consent screen, and land in your Pipedrive company. Returns straight away if you are already signed in, and reports the Pipedrive account and company it signed into. Optionally pass which Google account to use. Needs a browser that is already signed in to Google.

- Site: pipedrive.com
- Address: `reduck/pipedrive.com/login_with_google`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pipedrive.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `account` (string | null, optional)
- `workspace` (string | null, optional): Pipedrive company subdomain

## FAQ

### What does "Pipedrive login (Google SSO)" do?

Log into Pipedrive with the Google button, handling the Google account chooser and consent screen, and land in your Pipedrive company. Returns straight away if you are already signed in, and reports the Pipedrive account and company it signed into. Optionally pass which Google account to use. Needs a browser that is already signed in to Google.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn, workspace.

### Do I need to be logged in to pipedrive.com?

Yes. It acts as you on pipedrive.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the pipedrive.com cookies saved by the Reduck extension.

### Does it change anything on pipedrive.com, or only read data?

It makes changes on pipedrive.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pipedrive.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pipedrive.com/login_with_google
