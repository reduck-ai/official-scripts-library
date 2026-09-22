# Get Notion pricing plans

Automatically get Notion pricing plans on notion.so. Read Notion's public pricing page (notion.com/pricing): all plans (Free, Plus, Business, Enterprise) with price, billing unit, description, CTA, and feature list, for either monthly or yearly billing. Currency follows the site's own geo/session detection (not independently selectable) and is returned as `currency` so callers know what the prices are denominated in. No "monitor changes" affordance exists here or on the site itself — diff repeated get_pricing calls yourself if you need change tracking.

- Site: notion.so
- Address: `reduck/notion.so/get_pricing`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notion.so/get_pricing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notion.so/get_pricing
```

## Input

- `billing` (string, optional): Billing interval to price against, mirroring the site's own 'Pay monthly'/'Pay yearly' toggle. Yearly is the site's default view and shows per-month-equivalent pricing at the yearly discount.

## Output

- `plans` (array, required)
- `billing` (string, required)
- `currency` (string, required): 3-letter currency code active for this session (e.g. EUR, USD), as shown by the site's own currency selector. Not caller-controlled.

## FAQ

### What does "Get Notion pricing plans" do?

Read Notion's public pricing page (notion.com/pricing): all plans (Free, Plus, Business, Enterprise) with price, billing unit, description, CTA, and feature list, for either monthly or yearly billing. Currency follows the site's own geo/session detection (not independently selectable) and is returned as `currency` so callers know what the prices are denominated in. No "monitor changes" affordance exists here or on the site itself — diff repeated get_pricing calls yourself if you need change tracking.

### How do I automatically get Notion pricing plans on notion.so?

Ask an AI agent connected to Reduck to run reduck/notion.so/get_pricing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notion.so/get_pricing

### Is there a notion.so API to get Notion pricing plans?

You do not need one. "Get Notion pricing plans" drives the real notion.so pages in a browser, so it works whether or not notion.so offers an API for this.

### What information do I need to provide?

Optional: billing.

### What does it return?

It returns plans, billing, currency.

### Do I need to be logged in to notion.so?

No. It only uses pages of notion.so that are reachable without signing in.

### Does it change anything on notion.so, or only read data?

It only reads. It looks things up on notion.so and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notion.so/get_pricing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notion.so/get_pricing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/notion.so/get_pricing
