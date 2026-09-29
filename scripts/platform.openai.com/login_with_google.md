# OpenAI Platform login (Google SSO)

Log into the OpenAI API Platform (platform.openai.com) with Continue with Google, handling the Google account chooser and consent screen, and wait for OpenAI to finish the sign-in. Returns straight away if you are already signed in, and reports the account email and default organization. A Cloudflare check is waited out (never clicked) and named if it does not clear. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that already has an OpenAI account.

- Site: platform.openai.com
- Address: `reduck/platform.openai.com/login_with_google`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/platform.openai.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `account` (string | null, optional): OpenAI account email
- `organization` (string | null, optional): Default OpenAI organization name

## FAQ

### What does "OpenAI Platform login (Google SSO)" do?

Log into the OpenAI API Platform (platform.openai.com) with Continue with Google, handling the Google account chooser and consent screen, and wait for OpenAI to finish the sign-in. Returns straight away if you are already signed in, and reports the account email and default organization. A Cloudflare check is waited out (never clicked) and named if it does not clear. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that already has an OpenAI account.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn, organization.

### Do I need to be logged in to platform.openai.com?

Yes. It acts as you on platform.openai.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the platform.openai.com cookies saved by the Reduck extension.

### Does it change anything on platform.openai.com, or only read data?

It makes changes on platform.openai.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/platform.openai.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/platform.openai.com/login_with_google
