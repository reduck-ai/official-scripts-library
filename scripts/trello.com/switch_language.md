# Switch Trello account language

Automatically switch Trello account language on trello.com. Change the display language of your Trello account, via Atlassian's account-level language preference. Pass a locale code (e.g. "en_GB", "fr_FR", "de_DE", "it_IT", "es_ES"). Returns the language now active in Trello.

- Site: trello.com
- Address: `reduck/trello.com/switch_language`
- Updated: 2026-08-31 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trello.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trello.com/switch_language
```

## Input

- `locale` (string, required): Locale code, e.g. "en_GB", "en_US", "fr_FR", "de_DE", "it_IT", "es_ES".

## Output

- `locale` (string, required)

## FAQ

### What does "Switch Trello account language" do?

Change the display language of your Trello account, via Atlassian's account-level language preference. Pass a locale code (e.g. "en_GB", "fr_FR", "de_DE", "it_IT", "es_ES"). Returns the language now active in Trello.

### How do I automatically switch Trello account language on trello.com?

Ask an AI agent connected to Reduck to run reduck/trello.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trello.com/switch_language

### Is there a trello.com API to switch Trello account language?

You do not need one. "Switch Trello account language" drives the real trello.com pages in a browser, so it works whether or not trello.com offers an API for this.

### What information do I need to provide?

Required: locale.

### What does it return?

It returns locale.

### Do I need to be logged in to trello.com?

Yes. It acts as you on trello.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the trello.com cookies saved by the Reduck extension.

### Does it change anything on trello.com, or only read data?

It makes changes on trello.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trello.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trello.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trello.com/switch_language
