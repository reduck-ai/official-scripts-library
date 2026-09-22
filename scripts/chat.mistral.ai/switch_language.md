# Switch Le Chat display language

Automatically switch Le Chat display language on chat.mistral.ai. Change the signed-in Le Chat account's display language (Préférences), by its own native name (e.g. "English", "Français", "Deutsch", "Español", "Italiano"). Applies immediately, account-wide, and works starting from any current UI language.

- Site: chat.mistral.ai
- Address: `reduck/chat.mistral.ai/switch_language`
- Updated: 2026-08-26 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chat.mistral.ai/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/switch_language
```

## Input

- `language` (string, required): Target language by its own native name, exactly as Le Chat's language picker shows it (e.g. "English", "Français", "Deutsch", "Español", "Polski", "Italiano", "Português (Brasil)", "العربية", "Nederlands", "Українська")

## Output

- `changed` (boolean, required): Whether the language actually changed
- `newLanguage` (string, required)
- `languageCode` (string, required): The locale code Le Chat's own API applied (e.g. "en", "fr", "de")
- `previousLanguage` (string, required): The account's display language before this call, by its native name

## FAQ

### What does "Switch Le Chat display language" do?

Change the signed-in Le Chat account's display language (Préférences), by its own native name (e.g. "English", "Français", "Deutsch", "Español", "Italiano"). Applies immediately, account-wide, and works starting from any current UI language.

### How do I automatically switch Le Chat display language on chat.mistral.ai?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/switch_language

### Is there a chat.mistral.ai API to switch Le Chat display language?

You do not need one. "Switch Le Chat display language" drives the real chat.mistral.ai pages in a browser, so it works whether or not chat.mistral.ai offers an API for this.

### What information do I need to provide?

Required: language.

### What does it return?

It returns changed, newLanguage, languageCode, previousLanguage.

### Do I need to be logged in to chat.mistral.ai?

Yes. It acts as you on chat.mistral.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chat.mistral.ai cookies saved by the Reduck extension.

### Does it change anything on chat.mistral.ai, or only read data?

It makes changes on chat.mistral.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chat.mistral.ai/switch_language
