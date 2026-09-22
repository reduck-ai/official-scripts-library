# Set Claude.ai model and effort

Automatically set Claude.ai model and effort on claude.ai. Change the model and/or the effort level the Claude.ai composer uses for new chats, by id (from list_models). Pass model, effort, or both; the effort applies to the model selected once the change is made. The choice is saved to the account, so it holds across browsers and reloads. Returns the model and effort now selected as the site confirms them. A target that is already selected is left as is. Asking for an effort a model does not offer, or a model the picker does not list, fails with the available ids. Requires a signed-in session.

- Site: claude.ai
- Address: `reduck/claude.ai/set_model`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/set_model`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/set_model
```

## Input

- `model` (string, optional): Model id as list_models reports it, e.g. "claude-opus-5", "claude-sonnet-5", "claude-haiku-4-5-20251001".
- `effort` (string, optional): Effort level id. Not every model offers every level, and some (Haiku) offer none.

## Output

- `model` (string | null, required): Id of the model now selected.
- `effort` (string | null, required): Id of the effort level now selected for that model. Null when the model has no effort levels.

## FAQ

### What does "Set Claude.ai model and effort" do?

Change the model and/or the effort level the Claude.ai composer uses for new chats, by id (from list_models). Pass model, effort, or both; the effort applies to the model selected once the change is made. The choice is saved to the account, so it holds across browsers and reloads. Returns the model and effort now selected as the site confirms them. A target that is already selected is left as is. Asking for an effort a model does not offer, or a model the picker does not list, fails with the available ids. Requires a signed-in session.

### How do I automatically set Claude.ai model and effort on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/set_model, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/set_model

### Is there a claude.ai API to set Claude.ai model and effort?

You do not need one. "Set Claude.ai model and effort" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Optional: model, effort.

### What does it return?

It returns model, effort.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It makes changes on claude.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/set_model, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/set_model

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/set_model
