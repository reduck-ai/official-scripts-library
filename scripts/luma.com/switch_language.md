# Switch Luma account language

Automatically switch Luma account language on luma.com. Change the signed-in Luma account's display language via the account preferences page, by its native name (e.g. "English", "Français", "Deutsch", "Italiana", "Español"). Built to support locale testing of other Luma scripts.

- Site: luma.com
- Address: `reduck/luma.com/switch_language`
- Updated: 2026-08-31 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/switch_language
```

## Input

- `language` (string, required): The language's native display name as Luma lists it, e.g. "English", "Français", "Deutsch", "Italiana", "Español".

## Output

- `applied_language` (string, required)
- `previous_language` (string | null, optional)

## FAQ

### What does "Switch Luma account language" do?

Change the signed-in Luma account's display language via the account preferences page, by its native name (e.g. "English", "Français", "Deutsch", "Italiana", "Español"). Built to support locale testing of other Luma scripts.

### How do I automatically switch Luma account language on luma.com?

Ask an AI agent connected to Reduck to run reduck/luma.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/switch_language

### Is there a luma.com API to switch Luma account language?

You do not need one. "Switch Luma account language" drives the real luma.com pages in a browser, so it works whether or not luma.com offers an API for this.

### What information do I need to provide?

Required: language.

### What does it return?

It returns applied_language, previous_language.

### Do I need to be logged in to luma.com?

Yes. It acts as you on luma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the luma.com cookies saved by the Reduck extension.

### Does it change anything on luma.com, or only read data?

It makes changes on luma.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/switch_language
