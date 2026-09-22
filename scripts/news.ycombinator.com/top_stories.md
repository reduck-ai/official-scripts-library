# Top Hacker News stories

Read the top N stories from the Hacker News front page: rank, title, url, points, comments_count and a link to the discussion. The front page lists about 30 stories, so an n above that caps out rather than paginating. A story nobody has commented on yet reports 0 comments; YC job posts carry neither a score nor a discussion, so their points and comments_count are null. If Hacker News is throttling requests from your address, the script says so instead of returning a partial list.

- Site: news.ycombinator.com
- Address: `reduck/news.ycombinator.com/top_stories`
- Updated: 2026-09-17 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/news.ycombinator.com/top_stories`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/news.ycombinator.com/top_stories
```

## Input

- `n` (integer, optional)

## FAQ

### What does "Top Hacker News stories" do?

Read the top N stories from the Hacker News front page: rank, title, url, points, comments_count and a link to the discussion. The front page lists about 30 stories, so an n above that caps out rather than paginating. A story nobody has commented on yet reports 0 comments; YC job posts carry neither a score nor a discussion, so their points and comments_count are null. If Hacker News is throttling requests from your address, the script says so instead of returning a partial list.

### What information do I need to provide?

Optional: n.

### Do I need to be logged in to news.ycombinator.com?

No. It only uses pages of news.ycombinator.com that are reachable without signing in.

### Does it change anything on news.ycombinator.com, or only read data?

It only reads. It looks things up on news.ycombinator.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/news.ycombinator.com/top_stories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.ycombinator.com/top_stories

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/news.ycombinator.com/top_stories
