# Read your X (Twitter) For You timeline

Automatically read your X (Twitter) For You timeline on x.com. Get tweets from your personal For You home feed — the timeline as shown: top-level posts plus the replies and quote-tweets X threads in. Returns per tweet: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote, plus ref objects quoted_tweet/in_reply_to (each {id, author_handle}, null when N/A). For a repost, the tweet IS the reposted original as X shows it: id, author, text and counts are the original's, is_retweet is true, and reposted_by/reposted_at say who reposted it and when. in_reply_to != null is the reply test. Count is capped by how far the feed paginates before throttling.

- Site: x.com
- Address: `reduck/x.com/get_personal_feed`
- Updated: 2026-10-19 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_personal_feed`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_personal_feed
```

## Input

- `count` (integer, optional): How many to return. Without it, the script returns the first page X shows (often 20 to 40). With it, the script loads more until it has count, reaches the end, or X stops loading; complete says whether it reached the end.

## Output

- `count` (integer, required): Number of tweets returned. 0 is a valid answer.
- `tweets` (array, required)
- `complete` (boolean, required): True when X showed the end of the feed and every one it sent is returned. False when there may be more: count was reached, X stopped loading, or no count was given and the first page is not the end.

## FAQ

### What does "Read your X (Twitter) For You timeline" do?

Get tweets from your personal For You home feed — the timeline as shown: top-level posts plus the replies and quote-tweets X threads in. Returns per tweet: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote, plus ref objects quoted_tweet/in_reply_to (each {id, author_handle}, null when N/A). For a repost, the tweet IS the reposted original as X shows it: id, author, text and counts are the original's, is_retweet is true, and reposted_by/reposted_at say who reposted it and when. in_reply_to != null is the reply test. Count is capped by how far the feed paginates before throttling.

### How do I automatically read your X (Twitter) For You timeline on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_personal_feed, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_personal_feed

### Is there a x.com API to read your X (Twitter) For You timeline?

You do not need one. "Read your X (Twitter) For You timeline" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns count, tweets, complete.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_personal_feed, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_personal_feed

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_personal_feed
