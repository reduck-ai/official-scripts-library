# Get trending Reddit posts

Automatically get trending Reddit posts on reddit.com. List Reddit's trending threads from r/popular, one page at a time, with optional sort. Returns id, url, title, subreddit, author, score, comment count, date, post type and the post's text per thread. Each call returns one page as Reddit serves it (the first page can be short, a few threads) and a nextCursor: pass it as cursor, with the same sort, for the next page; it is null when the feed has no more.

- Site: reddit.com
- Address: `reduck/reddit.com/get_trending`
- Updated: 2026-10-22 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_trending`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_trending
```

## Input

- `sort` (string, optional): Feed sort. Omit for Reddit's default ranking.
- `cursor` (string, optional): The nextCursor of the previous answer, to read the next page. Omit for the first page. Pass the same sort as for the first page.

## Output

- `count` (number, required)
- `threads` (array, required)
- `nextCursor` (string | null, required): Pass as cursor to read the next page; null when the feed has no next page.

## FAQ

### What does "Get trending Reddit posts" do?

List Reddit's trending threads from r/popular, one page at a time, with optional sort. Returns id, url, title, subreddit, author, score, comment count, date, post type and the post's text per thread. Each call returns one page as Reddit serves it (the first page can be short, a few threads) and a nextCursor: pass it as cursor, with the same sort, for the next page; it is null when the feed has no more.

### How do I automatically get trending Reddit posts on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_trending, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_trending

### Is there a reddit.com API to get trending Reddit posts?

You do not need one. "Get trending Reddit posts" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Optional: sort, cursor.

### What does it return?

It returns count, threads, nextCursor.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

Unknown: its author has not declared whether it changes anything on reddit.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_trending, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_trending

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_trending
