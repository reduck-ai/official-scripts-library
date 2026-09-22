# Search a subreddit

Automatically search a subreddit on reddit.com. Search posts within a single subreddit, with optional sort, time window, and date cutoff. Returns subreddit, count, and threads (each with id, url, title, author, score, num_comments, created, subreddit, nsfw, preview_text). `limit` is a maximum, not a guarantee: a search with fewer matches returns what exists. With `sort=new`, pass `since` (an ISO date or shorthand like "7d") to filter out results older than that cutoff — useful for searching a subreddit for recent activity by date rather than by relevance/rank. When a query has no genuine matches, Reddit's own search sometimes silently returns a small number of loosely-related posts from the subreddit instead of an empty result, with no way to tell them apart from real hits — a non-zero count doesn't guarantee relevance. Reddit's subreddit-scoped search cards show titles only, with no body excerpt, so preview_text is null here on every sort; that is the surface, not a limitation of the script. To get per-subreddit results that include body excerpts, use reddit.com/search_reddit with a `subreddit:name` term in the query. Reddit caps each page at 100 results, so paginate with the after cursor to go beyond that.

- Site: reddit.com
- Address: `reduck/reddit.com/search_subreddit`
- Updated: 2026-09-03 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/search_subreddit`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_subreddit
```

## Input

- `topic` (string, required): Search query
- `subreddit` (string, required): Subreddit name, with or without the r/ prefix
- `sort` (string, optional): Reddit's native sort (default relevance)
- `time` (string, optional): Reddit's native time filter (default all). Ignored by Reddit when sort=new.
- `limit` (number, optional): Max results, paginating via the site's own infinite scroll (default 25)
- `since` (string, optional): sort:"new" only — filters out results older than this cutoff: ISO date ("2026-06-01") or shorthand ("24h", "7d", "2w").

## Output

- `count` (number, required)
- `threads` (array, required)
- `subreddit` (string, required)

## FAQ

### What does "Search a subreddit" do?

Search posts within a single subreddit, with optional sort, time window, and date cutoff. Returns subreddit, count, and threads (each with id, url, title, author, score, num_comments, created, subreddit, nsfw, preview_text). `limit` is a maximum, not a guarantee: a search with fewer matches returns what exists. With `sort=new`, pass `since` (an ISO date or shorthand like "7d") to filter out results older than that cutoff — useful for searching a subreddit for recent activity by date rather than by relevance/rank. When a query has no genuine matches, Reddit's own search sometimes silently returns a small number of loosely-related posts from the subreddit instead of an empty result, with no way to tell them apart from real hits — a non-zero count doesn't guarantee relevance. Reddit's subreddit-scoped search cards show titles only, with no body excerpt, so preview_text is null here on every sort; that is the surface, not a limitation of the script. To get per-subreddit results that include body excerpts, use reddit.com/search_reddit with a `subreddit:name` term in the query. Reddit caps each page at 100 results, so paginate with the after cursor to go beyond that.

### How do I automatically search a subreddit on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/search_subreddit, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_subreddit

### Is there a reddit.com API to search a subreddit?

You do not need one. "Search a subreddit" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: subreddit, topic. Optional: sort, time, limit, since.

### What does it return?

It returns count, threads, subreddit.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/search_subreddit, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_subreddit

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/search_subreddit
