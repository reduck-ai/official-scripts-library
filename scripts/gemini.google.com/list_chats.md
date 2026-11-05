# List Gemini chats

Automatically list Gemini chats on gemini.google.com. List your recent Gemini conversations (the sidebar's recent chats), newest first. Pass authuser to choose which Google account of this browser to read; it defaults to the first signed-in account. Signed out, the run fails and asks you to sign in.

- Site: gemini.google.com
- Address: `reduck/gemini.google.com/list_chats`
- Updated: 2026-11-04 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gemini.google.com/list_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/list_chats
```

## Input

- `authuser` (integer, optional): Which Google account of this browser to use: 0 = first signed-in account (the default), 1 = second, and so on.

## FAQ

### What does "List Gemini chats" do?

List your recent Gemini conversations (the sidebar's recent chats), newest first. Pass authuser to choose which Google account of this browser to read; it defaults to the first signed-in account. Signed out, the run fails and asks you to sign in.

### How do I automatically list Gemini chats on gemini.google.com?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/list_chats

### Is there a gemini.google.com API to list Gemini chats?

You do not need one. "List Gemini chats" drives the real gemini.google.com pages in a browser, so it works whether or not gemini.google.com offers an API for this.

### What information do I need to provide?

Optional: authuser.

### Do I need to be logged in to gemini.google.com?

Yes. It acts as you on gemini.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the gemini.google.com cookies saved by the Reduck extension.

### Does it change anything on gemini.google.com, or only read data?

It only reads. It looks things up on gemini.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/list_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/gemini.google.com/list_chats
