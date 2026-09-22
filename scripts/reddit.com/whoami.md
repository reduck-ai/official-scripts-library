# Who am I on Reddit

Report which Reddit account the browser is signed in as: the username (the u/ handle every other Reddit script takes as an argument) and the profile display name, which a redditor can set to something different. Throws when signed out. Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/whoami`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/whoami
```

## Input

It takes no input.

## Output

- `username` (string, required): The account's username without the u/ prefix, read off the URL /user/me resolved to — the identity every other script takes as an argument.
- `display_name` (string | null, required): The name shown on the profile header, which a redditor can set to something other than their username; equal to username when unset.

## FAQ

### What does "Who am I on Reddit" do?

Report which Reddit account the browser is signed in as: the username (the u/ handle every other Reddit script takes as an argument) and the profile display name, which a redditor can set to something different. Throws when signed out. Runs only via the browser extension, not the hosted cloud browser.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns username, display_name.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/whoami
