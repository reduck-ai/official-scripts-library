# Switch Discord display language

Automatically switch Discord display language on discord.com. Change the display language of the signed-in Discord account, via User Settings &gt; Language &amp; Time. Accepts en, fr, de, it and es, and reads the new setting back off the settings page so the result confirms the change rather than echoing the request. It works whatever language the account is currently displaying in. This changes account-level state for everyone using that account. Requires being logged in.

- Site: discord.com
- Address: `reduck/discord.com/switch_language`
- Updated: 2026-08-31 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/switch_language
```

## Input

- `language` (string, required): Target language: en (English, US), fr (Français), de (Deutsch), it (Italiano), es (Español).

## Output

- `language` (string, required)
- `confirmedNative` (string, required): The native language name now shown as selected, read back from the settings page.

## FAQ

### What does "Switch Discord display language" do?

Change the display language of the signed-in Discord account, via User Settings &gt; Language &amp; Time. Accepts en, fr, de, it and es, and reads the new setting back off the settings page so the result confirms the change rather than echoing the request. It works whatever language the account is currently displaying in. This changes account-level state for everyone using that account. Requires being logged in.

### How do I automatically switch Discord display language on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/switch_language

### Is there a discord.com API to switch Discord display language?

You do not need one. "Switch Discord display language" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: language.

### What does it return?

It returns language, confirmedNative.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/switch_language
