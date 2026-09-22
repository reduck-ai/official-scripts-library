# Notion display language switcher

Switch the display language for the current Notion account, via Settings > Preferences > Language. Supports fr, de, en, it, es.

- Site: notion.com
- Address: `reduck/notion.com/switch_language`
- Updated: 2026-09-01 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notion.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notion.com/switch_language
```

## Input

- `language` (string, required): Target display language.

## Output

- `language` (string, required)
- `alreadySet` (boolean, required)
- `docLang` (string, optional): document.documentElement.lang after the switch, waited for until it agrees with the requested language. On the already-set path the tab may have booted from Notion's cached shell still rendering the previous locale, so it is reloaded once before the guard gives up.

## FAQ

### What does "Notion display language switcher" do?

Switch the display language for the current Notion account, via Settings > Preferences > Language. Supports fr, de, en, it, es.

### What information do I need to provide?

Required: language.

### What does it return?

It returns docLang, language, alreadySet.

### Do I need to be logged in to notion.com?

Yes. It acts as you on notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the notion.com cookies saved by the Reduck extension.

### Does it change anything on notion.com, or only read data?

It makes changes on notion.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notion.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notion.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/notion.com/switch_language
