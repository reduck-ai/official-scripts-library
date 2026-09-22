# List ChatGPT models

Automatically list ChatGPT models on chatgpt.com. List the models ChatGPT offers the signed-in account and the lanes its model picker is built from, plus the account's default model. Each model carries its slug, title and description; each lane carries its id, name, default model, the models it holds and the plan it requires. On a free account the picker itself is not shown and only the Auto and Instant lanes come back, which is what the site offers there. Requires a signed-in session.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/list_models`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/list_models`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_models
```

## Input

It takes no input.

## Output

- `lanes` (array, required): The picker's lanes, in the order the site lists them.
- `models` (array, required)
- `defaultModel` (string | null, required): Slug of the account's default model, e.g. "auto".

## FAQ

### What does "List ChatGPT models" do?

List the models ChatGPT offers the signed-in account and the lanes its model picker is built from, plus the account's default model. Each model carries its slug, title and description; each lane carries its id, name, default model, the models it holds and the plan it requires. On a free account the picker itself is not shown and only the Auto and Instant lanes come back, which is what the site offers there. Requires a signed-in session.

### How do I automatically list ChatGPT models on chatgpt.com?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/list_models, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_models

### Is there a chatgpt.com API to list ChatGPT models?

You do not need one. "List ChatGPT models" drives the real chatgpt.com pages in a browser, so it works whether or not chatgpt.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns lanes, models, defaultModel.

### Do I need to be logged in to chatgpt.com?

Yes. It acts as you on chatgpt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chatgpt.com cookies saved by the Reduck extension.

### Does it change anything on chatgpt.com, or only read data?

It only reads. It looks things up on chatgpt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/list_models, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_models

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/list_models
