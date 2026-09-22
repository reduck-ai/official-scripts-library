# Get subreddit threads

Automatically get subreddit threads on reddit.com. List a subreddit's threads by Reddit's native sort (best/hot/new/top/rising). "new" is chronological (filter with `since`); "top" takes a `time` window (hour…all); others paginate by `limit`. Returns url, title, author, score, num_comments, created, post_type, and body — the post's full text (never truncated; null for link/image posts). `limit` is a maximum, not a guarantee: fewer matching threads returns what exists.

- Site: reddit.com
- Address: `reduck/reddit.com/get_subreddit_threads`
- Updated: 2026-09-11 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_subreddit_threads`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_subreddit_threads
```

## Input

- `subreddit` (string, required): Subreddit name, with or without the r/ prefix. Case-insensitive: Reddit redirects to the canonical casing (r/python -> r/Python) and the script follows it.
- `sort` (string, optional): Reddit's native subreddit sort. "new" is chronological (supports `since`); best/hot/top/rising are ranked (use `limit`). Default new.
- `time` (string, optional): Time window for sort:"top" only (default all). Rejected for other sorts.
- `limit` (number, optional): Max number of threads to return (newest first). Defaults to 25 when `since` is not given. With `since` and no `limit`, the time window is the only bound. A maximum, not a guarantee: fewer matching threads returns what exists.
- `since` (string, optional): sort:"new" only - how far back to go: ISO date ("2026-06-01") or shorthand ("24h", "7d", "2w"). Combine with `limit` to cap a time window.

## Output

- `count` (number, required)
- `threads` (array, required)
- `subreddit` (string, required)

## FAQ

### What does "Get subreddit threads" do?

List a subreddit's threads by Reddit's native sort (best/hot/new/top/rising). "new" is chronological (filter with `since`); "top" takes a `time` window (hour…all); others paginate by `limit`. Returns url, title, author, score, num_comments, created, post_type, and body — the post's full text (never truncated; null for link/image posts). `limit` is a maximum, not a guarantee: fewer matching threads returns what exists.

### How do I automatically get subreddit threads on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_subreddit_threads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_subreddit_threads

### Is there a reddit.com API to get subreddit threads?

You do not need one. "Get subreddit threads" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: subreddit. Optional: sort, time, limit, since.

### What does it return?

It returns count, threads, subreddit.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_subreddit_threads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_subreddit_threads

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_subreddit_threads
