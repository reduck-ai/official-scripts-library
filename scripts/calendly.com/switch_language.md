# Switch Calendly language

Automatically switch Calendly language on calendly.com. Change the display language of a Calendly account (English, French, Spanish, German, or Brazilian Portuguese). Built to support locale testing of other Calendly scripts. Requires an authenticated session.

- Site: calendly.com
- Address: `reduck/calendly.com/switch_language`
- Updated: 2026-08-31 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendly.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendly.com/switch_language
```

## Input

- `language` (string, required): Target language code: en (English), fr (French), es (Spanish), de (German), pt (Brazilian Portuguese).

## Output

- `language` (string, required): The document language tag (document.documentElement.lang) read back after the switch, confirming what actually applied.

## FAQ

### What does "Switch Calendly language" do?

Change the display language of a Calendly account (English, French, Spanish, German, or Brazilian Portuguese). Built to support locale testing of other Calendly scripts. Requires an authenticated session.

### How do I automatically switch Calendly language on calendly.com?

Ask an AI agent connected to Reduck to run reduck/calendly.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendly.com/switch_language

### Is there a calendly.com API to switch Calendly language?

You do not need one. "Switch Calendly language" drives the real calendly.com pages in a browser, so it works whether or not calendly.com offers an API for this.

### What information do I need to provide?

Required: language.

### What does it return?

It returns language.

### Do I need to be logged in to calendly.com?

No. It only uses pages of calendly.com that are reachable without signing in.

### Does it change anything on calendly.com, or only read data?

It makes changes on calendly.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendly.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendly.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendly.com/switch_language
