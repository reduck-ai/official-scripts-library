# Miro switch display language

Change the display language of the Miro sign-in page (and the account-level language preference it sets) to any of Miro's supported languages.

- Site: miro.com
- Address: `reduck/miro.com/switch_language`
- Updated: 2026-08-31 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/miro.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/miro.com/switch_language
```

## Input

- `language` (string, required): Language code to switch Miro's UI to.

## Output

- `url` (string, required)
- `language` (string, required)

## FAQ

### What does "Miro switch display language" do?

Change the display language of the Miro sign-in page (and the account-level language preference it sets) to any of Miro's supported languages.

### What information do I need to provide?

Required: language.

### What does it return?

It returns url, language.

### Do I need to be logged in to miro.com?

No. It only uses pages of miro.com that are reachable without signing in.

### Does it change anything on miro.com, or only read data?

It makes changes on miro.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/miro.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/miro.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/miro.com/switch_language
