# ChatGPT switch display language

Switch the ChatGPT web app's display language via Settings, for a signed-in account. Requires an active session.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/switch_language`
- Updated: 2026-08-31 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/switch_language
```

## Input

- `language` (string, required): Target display language: fr (French), de (German), en (English US), it (Italian), es (Spanish)

## Output

- `htmlLang` (string, required): The document's html[lang] attribute after switching, confirming the change took effect

## FAQ

### What does "ChatGPT switch display language" do?

Switch the ChatGPT web app's display language via Settings, for a signed-in account. Requires an active session.

### What information do I need to provide?

Required: language.

### What does it return?

It returns htmlLang.

### Do I need to be logged in to chatgpt.com?

Yes. It acts as you on chatgpt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chatgpt.com cookies saved by the Reduck extension.

### Does it change anything on chatgpt.com, or only read data?

It makes changes on chatgpt.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/switch_language
