# Get an n8n workflow template

Automatically get an n8n workflow template on n8n.io. Read one template of the n8n workflow gallery (n8n.io/workflows) by its id: name, url, full description (Markdown), creation and update dates, views, price and purchase link (price 0 or null for a free template), creator, categories, the community nodes it needs (a template with any runs on self-hosted n8n only), its complexity as the node count and the count of each node type (sticky notes included), the apps it uses, and the workflow itself (nodes and connections) as n8n imports it. A paid template's nodes come without their settings. Its view count comes from the template's own page and can be higher than the one n8n.io/search_templates sorts by. An id with no template fails with a clear message: get ids from n8n.io/search_templates.

- Site: n8n.io
- Address: `reduck/n8n.io/get_template`
- Updated: 2026-11-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/n8n.io/get_template`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/n8n.io/get_template
```

## Input

- `id` (integer, required): The template's id, as n8n.io/search_templates returns it, or the number at the start of its url (https://n8n.io/workflows/<id>-...).

## Output

- `id` (integer, required)
- `url` (string, required)
- `name` (string, required)
- `workflow` (object, required)
- `nodeCount` (integer, required)
- `nodeTypes` (array, required)
- `apps` (array, optional)
- `price` (number | null, optional): 0 or null for a free template.
- `views` (integer | null, optional)
- `creator` (object | null, optional)
- `createdAt` (string | null, optional)
- `updatedAt` (string | null, optional)
- `categories` (array, optional)
- `description` (string | null, optional): Markdown.
- `purchaseUrl` (string | null, optional)
- `recentViews` (integer | null, optional)
- `communityNodes` (array, optional): Node types from community packages.

## FAQ

### What does "Get an n8n workflow template" do?

Read one template of the n8n workflow gallery (n8n.io/workflows) by its id: name, url, full description (Markdown), creation and update dates, views, price and purchase link (price 0 or null for a free template), creator, categories, the community nodes it needs (a template with any runs on self-hosted n8n only), its complexity as the node count and the count of each node type (sticky notes included), the apps it uses, and the workflow itself (nodes and connections) as n8n imports it. A paid template's nodes come without their settings. Its view count comes from the template's own page and can be higher than the one n8n.io/search_templates sorts by. An id with no template fails with a clear message: get ids from n8n.io/search_templates.

### How do I automatically get an n8n workflow template on n8n.io?

Ask an AI agent connected to Reduck to run reduck/n8n.io/get_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/n8n.io/get_template

### Is there a n8n.io API to get an n8n workflow template?

You do not need one. "Get an n8n workflow template" drives the real n8n.io pages in a browser, so it works whether or not n8n.io offers an API for this.

### What information do I need to provide?

Required: id.

### What does it return?

It returns id, url, apps, name, price, views, creator, workflow, createdAt, nodeCount, nodeTypes, updatedAt, categories, description, purchaseUrl, recentViews, communityNodes.

### Do I need to be logged in to n8n.io?

No. It only uses pages of n8n.io that are reachable without signing in.

### Does it change anything on n8n.io, or only read data?

It only reads. It looks things up on n8n.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/n8n.io/get_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/n8n.io/get_template

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/n8n.io/get_template
