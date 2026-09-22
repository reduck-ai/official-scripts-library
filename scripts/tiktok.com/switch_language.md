# Switch TikTok display language

Automatically switch TikTok display language on tiktok.com. Change the logged-in TikTok account's display language via the account menu (More > Language), given the language's own native name (e.g. "Français", "Deutsch", "English (US)", "Italiano", "Español") as shown in TikTok's own language picker. Returns the resulting page language code so the caller can confirm the switch took effect.

- Site: tiktok.com
- Address: `reduck/tiktok.com/switch_language`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/switch_language
```

## Input

- `language` (string, required): Native name of the target language exactly as TikTok's language picker shows it, e.g. "Français", "Deutsch", "English (US)", "Italiano", "Español"

## Output

- `resultingLangCode` (string | null, required): document.documentElement.lang after the switch, e.g. "en", "de", "fr"

## FAQ

### What does "Switch TikTok display language" do?

Change the logged-in TikTok account's display language via the account menu (More > Language), given the language's own native name (e.g. "Français", "Deutsch", "English (US)", "Italiano", "Español") as shown in TikTok's own language picker. Returns the resulting page language code so the caller can confirm the switch took effect.

### How do I automatically switch TikTok display language on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/switch_language

### Is there a tiktok.com API to switch TikTok display language?

You do not need one. "Switch TikTok display language" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: language.

### What does it return?

It returns resultingLangCode.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/switch_language
