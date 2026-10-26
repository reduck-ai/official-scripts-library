# Search Reddit threads in a subreddit, with post text

Automatically search Reddit threads in a subreddit, with post text on reddit.com. Search one subreddit for a query and get one page of matching threads in Reddit's order, each with title, subreddit, permalink, upvotes, comment count, creation time, flair and the post's full text. Sort and time window are configurable; pass the returned after value to read the next page (null on the last one). Requires being signed in to Reddit. A subreddit that refuses the search (private, banned) fails with its HTTP status. To search several subreddits or queries, run the script once per pair.

- Site: reddit.com
- Address: `reduck/reddit.com/search_subreddit_threads`
- Updated: 2026-10-22 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/search_subreddit_threads`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_subreddit_threads
```

## Input

- `query` (string, required): Search text, in Reddit's search syntax.
- `subreddit` (string, required): Subreddit name, with or without the r/ prefix.
- `sort` (string, optional)
- `time` (string, optional)
- `after` (string, optional): Pass the after value of the previous answer to read the next page.
- `limit` (integer, optional): Threads per page.

## Output

- `after` (string | null, required): Cursor for the next page; null on the last page.
- `query` (string, required)
- `threads` (array, required)
- `subreddit` (string, required)
- `count` (integer, optional)

## FAQ

### What does "Search Reddit threads in a subreddit, with post text" do?

Search one subreddit for a query and get one page of matching threads in Reddit's order, each with title, subreddit, permalink, upvotes, comment count, creation time, flair and the post's full text. Sort and time window are configurable; pass the returned after value to read the next page (null on the last one). Requires being signed in to Reddit. A subreddit that refuses the search (private, banned) fails with its HTTP status. To search several subreddits or queries, run the script once per pair.

### How do I automatically search Reddit threads in a subreddit, with post text on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/search_subreddit_threads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_subreddit_threads

### Is there a reddit.com API to search Reddit threads in a subreddit, with post text?

You do not need one. "Search Reddit threads in a subreddit, with post text" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: subreddit, query. Optional: sort, time, after, limit.

### What does it return?

It returns after, count, query, threads, subreddit.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/search_subreddit_threads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/search_subreddit_threads

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/search_subreddit_threads
