# Figma login

Log into Figma via Google SSO, driving the OAuth popup and landing in the Figma files dashboard.

- Site: figma.com
- Address: `reduck/figma.com/login_with_google`
- Updated: 2026-10-02 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/figma.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/figma.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account. When the browser already has a Figma session belonging to someone else, the run is refused rather than signing that account out.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)
- `accountName` (string | null, optional)

## FAQ

### What does "Figma login" do?

Log into Figma via Google SSO, driving the OAuth popup and landing in the Figma files dashboard.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn, accountName.

### Do I need to be logged in to figma.com?

Yes. It acts as you on figma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the figma.com cookies saved by the Reduck extension.

### Does it change anything on figma.com, or only read data?

It makes changes on figma.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/figma.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/figma.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/figma.com/login_with_google
