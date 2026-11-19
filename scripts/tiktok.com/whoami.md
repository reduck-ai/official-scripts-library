# TikTok whoami (signed-in account)

Report which TikTok account this browser is signed in as: the username, name (nickname) and user id. When the browser is signed out, the run fails with a signed-out error asking you to sign in to tiktok.com.

- Site: tiktok.com
- Address: `reduck/tiktok.com/whoami`
- Updated: 2026-11-18 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `userId` (string | null, optional)
- `nickname` (string | null, optional)
- `username` (string | null, optional)

## FAQ

### What does "TikTok whoami (signed-in account)" do?

Report which TikTok account this browser is signed in as: the username, name (nickname) and user id. When the browser is signed out, the run fails with a signed-out error asking you to sign in to tiktok.com.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, userId, evidence, loggedIn, nickname, username.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/whoami
