# Search X users

Automatically search X users on x.com. Search X for accounts by keyword (the People tab). Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio.

- Site: x.com
- Address: `reduck/x.com/search_users`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/search_users`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/search_users
```

## Input

- `query` (string, required): Search keyword or phrase to match against account names/handles/bios, e.g. 'AI safety researcher'. Same raw query grammar as X's People search tab.
- `count` (integer, optional): Max accounts to return. Scrolls until count is met or results dry up. Default 20, max 100.

## Output

- `count` (integer, required): Number of accounts returned. 0 is a first-class outcome (no matches).
- `query` (string, required)
- `users` (array, required)

## FAQ

### What does "Search X users" do?

Search X for accounts by keyword (the People tab). Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio.

### How do I automatically search X users on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/search_users

### Is there a x.com API to search X users?

You do not need one. "Search X users" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count.

### What does it return?

It returns count, query, users.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/search_users

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/search_users
