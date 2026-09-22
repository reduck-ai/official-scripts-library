# Get Reddit home feed

Automatically get Reddit home feed on reddit.com. Get the signed-in account's own Reddit home feed (reddit.com/?feed=home) — its mix of subscribed communities and Reddit's recommendations, in the order the feed serves them, promoted slots included. Not r/popular: use get_trending for the cross-Reddit trending feed. Returns per item id, url, title, subreddit, author, created, score, num_comments, upvote_ratio, post_type, content_href, body, plus is_subscribed (the post comes from a community you joined, as opposed to a recommendation) and is_promoted (an ad slot). An ad carries no subreddit, since it is posted from a user profile rather than a community. sort takes the feed's own five orders; time is Reddit's window on the top sort. count is a maximum — a feed that stops loading returns what it served.

- Site: reddit.com
- Address: `reduck/reddit.com/get_feed`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_feed`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_feed
```

## Input

- `sort` (string, optional): The feed's own sort, as the home page's sort control exposes it. Default best, which is Reddit's own default.
- `time` (string, optional): Time window for the top sort (Reddit applies it to top only, and defaults to day when omitted). Ignored by the other sorts.
- `count` (integer, optional): Maximum items to collect by scrolling the feed. The home feed is effectively infinite, so this is the only bound; fewer come back when it stops serving.

## Output

- `count` (number, required): Number of items returned.
- `posts` (array, required)

## FAQ

### What does "Get Reddit home feed" do?

Get the signed-in account's own Reddit home feed (reddit.com/?feed=home) — its mix of subscribed communities and Reddit's recommendations, in the order the feed serves them, promoted slots included. Not r/popular: use get_trending for the cross-Reddit trending feed. Returns per item id, url, title, subreddit, author, created, score, num_comments, upvote_ratio, post_type, content_href, body, plus is_subscribed (the post comes from a community you joined, as opposed to a recommendation) and is_promoted (an ad slot). An ad carries no subreddit, since it is posted from a user profile rather than a community. sort takes the feed's own five orders; time is Reddit's window on the top sort. count is a maximum — a feed that stops loading returns what it served.

### How do I automatically get Reddit home feed on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_feed, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_feed

### Is there a reddit.com API to get Reddit home feed?

You do not need one. "Get Reddit home feed" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Optional: sort, time, count.

### What does it return?

It returns count, posts.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_feed, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_feed

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_feed
