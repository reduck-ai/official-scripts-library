# Get trending Reddit posts

Automatically get trending Reddit posts on reddit.com. List Reddit's trending threads from the r/popular (or r/all) feed, with optional sort. Returns url, title, subreddit, author, score, comment count, date and displayed text per thread.

- Site: reddit.com
- Address: `reduck/reddit.com/get_trending`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_trending`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_trending
```

## Input

- `feed` (string, optional): Which cross-Reddit feed (default popular)
- `sort` (string, optional): Feed sort. Omit for Reddit's default ranking.
- `limit` (number, optional): Max threads to return (default 25), paginating via the feed's infinite scroll

## Output

- `count` (number, required)
- `threads` (array, required)
- `feed` (string, optional)

## FAQ

### What does "Get trending Reddit posts" do?

List Reddit's trending threads from the r/popular (or r/all) feed, with optional sort. Returns url, title, subreddit, author, score, comment count, date and displayed text per thread.

### How do I automatically get trending Reddit posts on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_trending, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_trending

### Is there a reddit.com API to get trending Reddit posts?

You do not need one. "Get trending Reddit posts" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Optional: feed, sort, limit.

### What does it return?

It returns feed, count, threads.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

Unknown: its author has not declared whether it changes anything on reddit.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_trending, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_trending

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_trending
