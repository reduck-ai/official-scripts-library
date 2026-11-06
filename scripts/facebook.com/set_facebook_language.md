# Set the Facebook account language

Automatically set the Facebook account language on facebook.com. Change the interface language of the signed-in Facebook account, picking it by its native name exactly as Facebook lists it (for example English (US) or Français (France)). Returns the language that was selected before and the one selected now, and fails with the list of available names when the requested one does not exist. The change applies to the whole account, including emails and notifications, until it is changed again.

- Site: facebook.com
- Address: `reduck/facebook.com/set_facebook_language`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/set_facebook_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/set_facebook_language
```

## Input

- `language` (string, required): Native name of the language as Facebook lists it, e.g. English (US), Français (France), Español.

## Output

- `changed` (boolean, required)
- `current` (string, required)
- `previous` (string | null, required)

## FAQ

### What does "Set the Facebook account language" do?

Change the interface language of the signed-in Facebook account, picking it by its native name exactly as Facebook lists it (for example English (US) or Français (France)). Returns the language that was selected before and the one selected now, and fails with the list of available names when the requested one does not exist. The change applies to the whole account, including emails and notifications, until it is changed again.

### How do I automatically set the Facebook account language on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/set_facebook_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/set_facebook_language

### Is there a facebook.com API to set the Facebook account language?

You do not need one. "Set the Facebook account language" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: language.

### What does it return?

It returns changed, current, previous.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/set_facebook_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/set_facebook_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/set_facebook_language
