# List today's Product Hunt launches

Automatically list today's Product Hunt launches on producthunt.com. List every product launching today on the Product Hunt homepage, in the order the page ranks them: rank, name, tagline, product slug, launch slug, launch URL (usable with get_launch_comments and post_launch_comment), launch-day score and comment count.

- Site: producthunt.com
- Address: `reduck/producthunt.com/list_today_launches`
- Updated: 2026-11-17 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/list_today_launches`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/list_today_launches
```

## Input

It takes no input.

## Output

- `launches` (array, required)

## FAQ

### What does "List today's Product Hunt launches" do?

List every product launching today on the Product Hunt homepage, in the order the page ranks them: rank, name, tagline, product slug, launch slug, launch URL (usable with get_launch_comments and post_launch_comment), launch-day score and comment count.

### How do I automatically list today's Product Hunt launches on producthunt.com?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/list_today_launches, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/list_today_launches

### Is there a producthunt.com API to list today's Product Hunt launches?

You do not need one. "List today's Product Hunt launches" drives the real producthunt.com pages in a browser, so it works whether or not producthunt.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns launches.

### Do I need to be logged in to producthunt.com?

No. It only uses pages of producthunt.com that are reachable without signing in.

### Does it change anything on producthunt.com, or only read data?

It only reads. It looks things up on producthunt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/list_today_launches, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/list_today_launches

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/list_today_launches
