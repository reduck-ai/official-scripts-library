# Get Notion Marketplace custom agent

Automatically get Notion Marketplace custom agent on app.notion.com. Fetch one Notion Marketplace custom agent by its URL slug: title, icon, brief and full description, advertised features, gallery images, categories, the integrations it requires (Notion, Slack, …), creator, install count, rating, price, published locales and last update. Read-only.

- Site: app.notion.com
- Address: `reduck/app.notion.com/get_marketplace_agent`
- Updated: 2026-08-21 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/get_marketplace_agent`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/get_marketplace_agent
```

## Input

- `slug` (string, required): The agent's URL slug, i.e. the last segment of app.notion.com/marketplace/custom-agents/<slug> (e.g. "weekly-meal-plan"). list_marketplace_agents returns it.
- `locale` (string, optional): Which published locale to read. Falls back to the agent's first published locale. Default "en-US".

## Output

- `id` (string, required)
- `url` (string, required)
- `slug` (string, required)
- `icon` (string | null, optional): Emoji, or an image URL for avatar icons.
- `price` (number | null, optional): 0 for the free agents.
- `title` (string | null, optional)
- `images` (array, optional): Gallery image URLs.
- `rating` (number | null, optional)
- `creator` (any, optional)
- `locales` (array, optional)
- `features` (array, optional): Capability keys listed under the title, e.g. creates_pages, responds_to_slack_mentions.
- `updatedAt` (string | null, optional): ISO timestamp of the published version's last edit.
- `categories` (array, optional): Category names shown in Details.
- `description` (string | null, optional): The About section.
- `ratingCount` (integer | null, optional)
- `installCount` (integer | null, optional): Downloads.
- `requirements` (array, optional): The integrations the agent needs (the Requirements section).
- `briefDescription` (string | null, optional): The one-line pitch under the title.

## FAQ

### What does "Get Notion Marketplace custom agent" do?

Fetch one Notion Marketplace custom agent by its URL slug: title, icon, brief and full description, advertised features, gallery images, categories, the integrations it requires (Notion, Slack, …), creator, install count, rating, price, published locales and last update. Read-only.

### How do I automatically get Notion Marketplace custom agent on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/get_marketplace_agent, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/get_marketplace_agent

### Is there a app.notion.com API to get Notion Marketplace custom agent?

You do not need one. "Get Notion Marketplace custom agent" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: slug. Optional: locale.

### What does it return?

It returns id, url, icon, slug, price, title, images, rating, creator, locales, features, updatedAt, categories, description, ratingCount, installCount, requirements, briefDescription.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/get_marketplace_agent, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/get_marketplace_agent

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/get_marketplace_agent
