# Search Instagram users

Automatically search Instagram users on instagram.com. Search Instagram accounts by keyword (name or handle). Returns ranked users with pk, username, full_name, is_private, is_verified, is_business, and profile_pic_url. Results are Instagram's own ranking; count is a hint the server may not honor exactly.

- Site: instagram.com
- Address: `reduck/instagram.com/search_users`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/search_users`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/search_users
```

## Input

- `query` (string, required): Search term — a name or handle, e.g. "nasa" or "marie dupont".
- `count` (integer, optional): Max users to return (server ranking hint).

## FAQ

### What does "Search Instagram users" do?

Search Instagram accounts by keyword (name or handle). Returns ranked users with pk, username, full_name, is_private, is_verified, is_business, and profile_pic_url. Results are Instagram's own ranking; count is a hint the server may not honor exactly.

### How do I automatically search Instagram users on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/search_users

### Is there a instagram.com API to search Instagram users?

You do not need one. "Search Instagram users" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

Unknown: its author has not declared whether it changes anything on instagram.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/search_users

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/search_users
