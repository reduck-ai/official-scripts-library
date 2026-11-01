# List n8n Community forum categories

Automatically list n8n Community forum categories on community.n8n.io. List every category of the n8n Community forum (community.n8n.io), subcategories included, in the order the forum shows them. Returns per category its id, name, slug, url, description, parentId (null for a top-level category) and its topic and post counts. Pass a category's id or url to community.n8n.io/get_category_threads to read its threads.

- Site: community.n8n.io
- Address: `reduck/community.n8n.io/list_categories`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/community.n8n.io/list_categories`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/community.n8n.io/list_categories
```

## Input

It takes no input.

## Output

- `categories` (array, required)

## FAQ

### What does "List n8n Community forum categories" do?

List every category of the n8n Community forum (community.n8n.io), subcategories included, in the order the forum shows them. Returns per category its id, name, slug, url, description, parentId (null for a top-level category) and its topic and post counts. Pass a category's id or url to community.n8n.io/get_category_threads to read its threads.

### How do I automatically list n8n Community forum categories on community.n8n.io?

Ask an AI agent connected to Reduck to run reduck/community.n8n.io/list_categories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/community.n8n.io/list_categories

### Is there a community.n8n.io API to list n8n Community forum categories?

You do not need one. "List n8n Community forum categories" drives the real community.n8n.io pages in a browser, so it works whether or not community.n8n.io offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns categories.

### Do I need to be logged in to community.n8n.io?

No. It only uses pages of community.n8n.io that are reachable without signing in.

### Does it change anything on community.n8n.io, or only read data?

It only reads. It looks things up on community.n8n.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/community.n8n.io/list_categories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/community.n8n.io/list_categories

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/community.n8n.io/list_categories
