# Search Reddit

Automatically search Reddit on reddit.com. Search posts across all of Reddit (no subreddit restriction), with optional sort and time window. Returns count and threads (each with id, url, title, author, subreddit, score, num_comments, created, nsfw, preview_text). `limit` is a maximum: fewer matching posts than requested returns however many exist. Useful to discover which subreddits discuss a topic. The sort changes how relevant the results are: `top` orders Reddit's matches by score, and because Reddit matches loosely, a heavily upvoted post only tangentially related to the query can outrank the genuine matches. That is Reddit's own ranking, returned as-is. Use the default `relevance` sort when on-topic results matter, and treat a non-zero count under `top` as "Reddit returned something", not as proof the posts are about the topic. Reddit refuses connections from datacenter addresses, so this works as-is on your own browser; on a hosted cloud browser the session has to be given a country so it exits through a residential address, otherwise Reddit blocks it and the script says so.

- Site: reddit.com
- Address: `reduck/reddit.com/search_reddit`
- Updated: 2026-09-15 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/search_reddit`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_reddit
```

## Input

- `sort` (string, optional): Reddit's native sort (default relevance)
- `time` (string, optional): Reddit's native time filter (default all). Ignored by Reddit when sort=new.
- `limit` (number, optional): Max results, paginating via the site's own infinite scroll (default 25)
- `query` (string, optional): Alias for `topic` (accepted for compatibility — prefer `topic`).
- `topic` (string, optional): Search query. Canonical name for this field; `query` is accepted as an alias.

## Output

- `count` (number, required)
- `threads` (array, required)

## FAQ

### What does "Search Reddit" do?

Search posts across all of Reddit (no subreddit restriction), with optional sort and time window. Returns count and threads (each with id, url, title, author, subreddit, score, num_comments, created, nsfw, preview_text). `limit` is a maximum: fewer matching posts than requested returns however many exist. Useful to discover which subreddits discuss a topic. The sort changes how relevant the results are: `top` orders Reddit's matches by score, and because Reddit matches loosely, a heavily upvoted post only tangentially related to the query can outrank the genuine matches. That is Reddit's own ranking, returned as-is. Use the default `relevance` sort when on-topic results matter, and treat a non-zero count under `top` as "Reddit returned something", not as proof the posts are about the topic. Reddit refuses connections from datacenter addresses, so this works as-is on your own browser; on a hosted cloud browser the session has to be given a country so it exits through a residential address, otherwise Reddit blocks it and the script says so.

### How do I automatically search Reddit on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/search_reddit, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_reddit

### Is there a reddit.com API to search Reddit?

You do not need one. "Search Reddit" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Optional: sort, time, limit, query, topic.

### What does it return?

It returns count, threads.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/search_reddit, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_reddit

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/search_reddit
