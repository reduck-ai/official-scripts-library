# Search TikTok users

Automatically search TikTok users on tiktok.com. Search TikTok accounts by keyword. Returns the top ~10 matches (TikTok web caps user search; not deeply paginable).

- Site: tiktok.com
- Address: `reduck/tiktok.com/search_users`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/search_users`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_users
```

## Input

- `query` (string, required): Search keyword(s) — name or handle fragment.

## Output

- `query` (string, required)
- `total` (integer, required): Number of users returned (TikTok web caps this around 10 per query; the endpoint's has_more/count/offset are non-functional for this surface, so there is no deeper page).
- `users` (array, required)

## FAQ

### What does "Search TikTok users" do?

Search TikTok accounts by keyword. Returns the top ~10 matches (TikTok web caps user search; not deeply paginable).

### How do I automatically search TikTok users on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_users

### Is there a tiktok.com API to search TikTok users?

You do not need one. "Search TikTok users" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns query, total, users.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

Unknown: its author has not declared whether it changes anything on tiktok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_users

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/search_users
