# List Claude.ai models and effort levels

Automatically list Claude.ai models and effort levels on claude.ai. List the models the Claude.ai composer offers, the effort levels available for the selected model, and which of each is currently selected. Models come back with their id, their display name and whether they sit in the picker's main list or under "More models". Effort levels are empty when the selected model has none (Haiku, for example, only offers an extended-thinking switch). Requires a signed-in session. Feed a model or effort id to set_model.

- Site: claude.ai
- Address: `reduck/claude.ai/list_models`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/list_models`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_models
```

## Input

It takes no input.

## Output

- `model` (string | null, required): Id of the selected model, e.g. "claude-opus-5".
- `effort` (string | null, required): Id of the selected effort level (low, medium, high, xhigh, max). Null when the selected model has no effort levels.
- `models` (array, required)
- `effortLevels` (array, required): Effort levels the selected model offers, in the picker's order. Empty when it has none.

## FAQ

### What does "List Claude.ai models and effort levels" do?

List the models the Claude.ai composer offers, the effort levels available for the selected model, and which of each is currently selected. Models come back with their id, their display name and whether they sit in the picker's main list or under "More models". Effort levels are empty when the selected model has none (Haiku, for example, only offers an extended-thinking switch). Requires a signed-in session. Feed a model or effort id to set_model.

### How do I automatically list Claude.ai models and effort levels on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_models, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_models

### Is there a claude.ai API to list Claude.ai models and effort levels?

You do not need one. "List Claude.ai models and effort levels" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns model, effort, models, effortLevels.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_models, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_models

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/list_models
