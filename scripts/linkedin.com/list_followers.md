# LinkedIn — list followers

Automatically list followers on linkedin.com. List the people who follow the signed-in LinkedIn member (My Network → Followers): each follower's profile URL, profile id, name and headline. LinkedIn links followers by member id (ACoAA…) rather than vanity slug on this page — the URL works either way. Scrolls to load more, up to `limit` (default 100, max 500), and says when it was truncated. Read-only; signed out is a clear error.

- Site: linkedin.com
- Address: `reduck/linkedin.com/list_followers`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/list_followers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_followers
```

## Input

- `limit` (integer, optional): Maximum entries to return (default 100).

## Output

- `count` (integer, required)
- `followers` (array, required)
- `truncated` (boolean, optional): True when `limit` was reached before the list ended.

## FAQ

### What does "LinkedIn — list followers" do?

List the people who follow the signed-in LinkedIn member (My Network → Followers): each follower's profile URL, profile id, name and headline. LinkedIn links followers by member id (ACoAA…) rather than vanity slug on this page — the URL works either way. Scrolls to load more, up to `limit` (default 100, max 500), and says when it was truncated. Read-only; signed out is a clear error.

### How do I automatically list followers on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/list_followers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_followers

### Is there a linkedin.com API to list followers?

You do not need one. "LinkedIn — list followers" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns count, followers, truncated.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/list_followers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_followers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/list_followers
