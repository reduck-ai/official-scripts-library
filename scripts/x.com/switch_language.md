# Switch X display language

Automatically switch X display language on x.com. Change the display language for the signed-in X (Twitter) account, under Settings > Accessibility, display, and languages > Languages. Takes an X locale code (e.g. fr, de, en, it, es, en-gb, zh-cn) and applies it immediately — the account's interface language changes account-wide until switched again. This only affects X's own UI text (menus, buttons), not the language of tweets in your timeline.

- Site: x.com
- Address: `reduck/x.com/switch_language`
- Updated: 2026-08-26 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/switch_language
```

## Input

- `locale` (string, required): X locale code to switch the account's display language to, e.g. "fr", "de", "en", "it", "es" (also accepts region/script variants X exposes, like "en-gb", "zh-cn", "ar-x-fm").

## Output

- `label` (string, required): The language's display name as shown in the selector, e.g. "French - français".
- `locale` (string, required)
- `was_already` (boolean, required): True if the account's display language already matched the requested locale before this call.
- `verified_on_page` (boolean, required): True if the page was re-inspected after the change and the display language is now confirmed set to the requested locale.

## FAQ

### What does "Switch X display language" do?

Change the display language for the signed-in X (Twitter) account, under Settings > Accessibility, display, and languages > Languages. Takes an X locale code (e.g. fr, de, en, it, es, en-gb, zh-cn) and applies it immediately — the account's interface language changes account-wide until switched again. This only affects X's own UI text (menus, buttons), not the language of tweets in your timeline.

### How do I automatically switch X display language on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/switch_language

### Is there a x.com API to switch X display language?

You do not need one. "Switch X display language" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: locale.

### What does it return?

It returns label, locale, was_already, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/switch_language
