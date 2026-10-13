# Get a tweet and its replies on X (Twitter)

Automatically get a tweet and its replies on X (Twitter) on x.com. Fetch a tweet by URL — the focal post plus the surrounding conversation. Returns `tweet` (the focal post; null if deleted/tombstoned) and `replies[]`, which holds every other tweet on the conversation page: both the focal's ancestors (the thread above it, present when the focal is itself a reply; each has `in_reply_to` null or pointing above the focal) and the replies below it (`in_reply_to` points at the focal or a sibling reply). Use `in_reply_to` to tell ancestors from replies and rebuild the thread — the array is not filtered to descendants of the focal. Each entry is a canonical tweet record: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote, in_reply_to {id, author_handle}. Scrolls the main thread until `count` is met (then complete=false — more may exist) or it drains (complete=true). Replies behind a "Show more replies"/hidden/probable-spam cursor are not expanded, so even complete=true is a floor, not a guarantee every nested reply was seen.

- Site: x.com
- Address: `reduck/x.com/get_tweet`
- Updated: 2026-10-12 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_tweet
```

## Input

- `tweet_url` (string, required): Full URL of the tweet, e.g. https://x.com/handle/status/123
- `sort` (string, optional): Order of the replies, as in the page's Sort replies menu: relevance (X's default ranking), recency (newest first) or likes (most liked first).
- `count` (integer, optional): How many replies to return. Without it, the script returns the first page X shows (often 20 to 40). With it, the script loads more until it has count, reaches the end, or X stops loading; complete says whether it reached the end.

## Output

- `count` (integer, required): Number of replies returned. 0 is a valid answer.
- `tweet` (object, required): The tweet at tweet_url. A deleted or unavailable tweet is an error.
- `replies` (array, required)
- `complete` (boolean, required): True when X showed the end of the conversation and every reply it sent is returned. False when there may be more. Replies behind "Show replies" are not opened, so true is a floor.
- `tweet_id` (string, required)

## FAQ

### What does "Get a tweet and its replies on X (Twitter)" do?

Fetch a tweet by URL — the focal post plus the surrounding conversation. Returns `tweet` (the focal post; null if deleted/tombstoned) and `replies[]`, which holds every other tweet on the conversation page: both the focal's ancestors (the thread above it, present when the focal is itself a reply; each has `in_reply_to` null or pointing above the focal) and the replies below it (`in_reply_to` points at the focal or a sibling reply). Use `in_reply_to` to tell ancestors from replies and rebuild the thread — the array is not filtered to descendants of the focal. Each entry is a canonical tweet record: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote, in_reply_to {id, author_handle}. Scrolls the main thread until `count` is met (then complete=false — more may exist) or it drains (complete=true). Replies behind a "Show more replies"/hidden/probable-spam cursor are not expanded, so even complete=true is a floor, not a guarantee every nested reply was seen.

### How do I automatically get a tweet and its replies on X (Twitter) on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_tweet

### Is there a x.com API to get a tweet and its replies on X (Twitter)?

You do not need one. "Get a tweet and its replies on X (Twitter)" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: tweet_url. Optional: sort, count.

### What does it return?

It returns count, tweet, replies, complete, tweet_id.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_tweet
