# Who am I (ChatGPT)

Report which ChatGPT account the browser is signed into: id, name, email, picture, identity provider — or loggedIn:false when the browser is anonymous. Reads the session endpoint the app itself hydrates auth from; never returns the session's access token.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/who_am_i`
- Updated: 2026-09-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/who_am_i`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/who_am_i
```

## Input

It takes no input.

## Output

- `user` (object | null, required): The signed-in account; null when the browser is anonymous.
- `loggedIn` (boolean, required)

## FAQ

### What does "Who am I (ChatGPT)" do?

Report which ChatGPT account the browser is signed into: id, name, email, picture, identity provider — or loggedIn:false when the browser is anonymous. Reads the session endpoint the app itself hydrates auth from; never returns the session's access token.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns user, loggedIn.

### Do I need to be logged in to chatgpt.com?

No. It only uses pages of chatgpt.com that are reachable without signing in.

### Does it change anything on chatgpt.com, or only read data?

It only reads. It looks things up on chatgpt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/who_am_i, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/who_am_i

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/who_am_i
