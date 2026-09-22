# List Notion Marketplace custom agents

Automatically list Notion Marketplace custom agents on app.notion.com. List the custom agents published on the Notion Marketplace (app.notion.com/marketplace/custom-agents). Returns the total count and one page of agents, each with id, slug, url, title, briefDescription, icon, features, installCount, rating and updatedAt. Order by "popular" (default) or "recent"; paginate with limit/offset. Read-only.

- Site: app.notion.com
- Address: `reduck/app.notion.com/list_marketplace_agents`
- Updated: 2026-08-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/list_marketplace_agents`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_marketplace_agents
```

## Input

- `limit` (integer, optional): Agents per page. The site itself asks for 50. Default 50.
- `locale` (string, optional): Listing locale, e.g. "en-US" (the site's default). Agents are published per locale.
- `offset` (integer, optional): Zero-based offset into the result set; page N = (N-1) * limit. Default 0.
- `orderBy` (string, optional): Marketplace ordering. Only these two are accepted by the site. Default "popular".

## Output

- `url` (string, required)
- `limit` (integer, required)
- `agents` (array, required)
- `offset` (integer, required)
- `hasMore` (boolean, required): True when the page came back full, i.e. there is probably another page at offset + limit.
- `count` (integer | null, optional): The marketplace's own estimate — it undercounts (reported 116 while offset paging reached 270 agents). Trust hasMore, not this, to know when to stop.

## FAQ

### What does "List Notion Marketplace custom agents" do?

List the custom agents published on the Notion Marketplace (app.notion.com/marketplace/custom-agents). Returns the total count and one page of agents, each with id, slug, url, title, briefDescription, icon, features, installCount, rating and updatedAt. Order by "popular" (default) or "recent"; paginate with limit/offset. Read-only.

### How do I automatically list Notion Marketplace custom agents on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/list_marketplace_agents, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_marketplace_agents

### Is there a app.notion.com API to list Notion Marketplace custom agents?

You do not need one. "List Notion Marketplace custom agents" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Optional: limit, locale, offset, orderBy.

### What does it return?

It returns url, count, limit, agents, offset, hasMore.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/list_marketplace_agents, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_marketplace_agents

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/list_marketplace_agents
