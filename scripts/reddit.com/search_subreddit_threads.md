# Search Reddit threads across several subreddits with a list of queries

Automatically search Reddit threads across several subreddits with a list of queries on reddit.com. Run several search queries across one or more subreddits in a single pass and get back the matching threads, deduplicated across queries and subreddits: title, subreddit, permalink, upvotes, comment count, creation date, flair, and the opening of the post body. Each thread also lists which of your queries matched it, and results are ordered by how many queries matched, then by upvotes. Sort and time window are configurable, and any query that a subreddit refuses is reported separately instead of failing the whole run.

- Site: reddit.com
- Address: `reduck/reddit.com/search_subreddit_threads`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/search_subreddit_threads`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_subreddit_threads
```

## Input

- `queries` (array, required)
- `subreddits` (array, required): Subreddit names without r/
- `sort` (string, optional)
- `time` (string, optional)
- `limit` (number, optional)
- `bodyChars` (number, optional)

## Output

- `count` (number, optional)
- `errors` (array, optional)
- `threads` (array, optional)

## FAQ

### What does "Search Reddit threads across several subreddits with a list of queries" do?

Run several search queries across one or more subreddits in a single pass and get back the matching threads, deduplicated across queries and subreddits: title, subreddit, permalink, upvotes, comment count, creation date, flair, and the opening of the post body. Each thread also lists which of your queries matched it, and results are ordered by how many queries matched, then by upvotes. Sort and time window are configurable, and any query that a subreddit refuses is reported separately instead of failing the whole run.

### How do I automatically search Reddit threads across several subreddits with a list of queries on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/search_subreddit_threads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_subreddit_threads

### Is there a reddit.com API to search Reddit threads across several subreddits with a list of queries?

You do not need one. "Search Reddit threads across several subreddits with a list of queries" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: subreddits, queries. Optional: sort, time, limit, bodyChars.

### What does it return?

It returns count, errors, threads.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/search_subreddit_threads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_subreddit_threads

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/search_subreddit_threads
