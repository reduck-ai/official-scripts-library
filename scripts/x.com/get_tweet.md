# Get a tweet and its replies on X (Twitter)

Automatically get a tweet and its replies on X (Twitter) on x.com. Get a tweet on X (Twitter) by URL, with the conversation around it: `tweet` (the post itself) and `replies` (every other post of its conversation on the page: the thread above it when it is a reply, and the replies below; use in_reply_to to rebuild the thread). Each post has id, url, author, text, created_at, lang, counts, in_reply_to and quoted_tweet. With count, it loads more replies until it has count or X reaches the end. complete is true only when X reached the end and left no folded replies (Show replies, hidden or probable-spam sections), which this script does not open. A deleted or unavailable tweet is an error. Requires being signed in to X.

- Site: x.com
- Address: `reduck/x.com/get_tweet`
- Updated: 2026-10-16 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_tweet
```

## Input

- `sort` (string, optional): Order of the replies, as in the page's Sort replies menu: relevance (X's default ranking), recency (newest first) or likes (most liked first).
- `count` (integer, optional): How many replies to return. Without it, the script returns the first page X shows (often 20 to 40). With it, the script loads more until it has count, reaches the end, or X stops loading; complete says whether it reached the end.
- `tweet_url` (string, optional): Full URL of the tweet, e.g. https://x.com/handle/status/123. Pass this or tweet_urls.
- `tweet_urls` (array, optional): Several tweet URLs (max 10), read one after another in the same page, instead of tweet_url. sort and count apply to each. Returns {results}, one per URL in order, each with error null or what went wrong. A rate limit, lock or sign-in wall stops the batch: the remaining URLs carry that error.

## Output

- `count` (integer, optional): Number of replies returned. 0 is a valid answer.
- `tweet` (any, optional): The tweet at tweet_url. A deleted or unavailable tweet is an error.
- `replies` (array, optional)
- `results` (array, optional): With tweet_urls only: one result per URL, in order, with the same fields as a single answer (tweet, tweet_id, count, complete, replies) plus tweet_url and error. When error is set, only tweet_url and error are present.
- `complete` (boolean, optional): True when X showed the end of the conversation and every reply it sent is returned. False when there may be more. Replies behind "Show replies" are not opened, so true is a floor.
- `tweet_id` (string, optional)

## FAQ

### What does "Get a tweet and its replies on X (Twitter)" do?

Get a tweet on X (Twitter) by URL, with the conversation around it: `tweet` (the post itself) and `replies` (every other post of its conversation on the page: the thread above it when it is a reply, and the replies below; use in_reply_to to rebuild the thread). Each post has id, url, author, text, created_at, lang, counts, in_reply_to and quoted_tweet. With count, it loads more replies until it has count or X reaches the end. complete is true only when X reached the end and left no folded replies (Show replies, hidden or probable-spam sections), which this script does not open. A deleted or unavailable tweet is an error. Requires being signed in to X.

### How do I automatically get a tweet and its replies on X (Twitter) on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_tweet

### Is there a x.com API to get a tweet and its replies on X (Twitter)?

You do not need one. "Get a tweet and its replies on X (Twitter)" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Optional: sort, count, tweet_url, tweet_urls.

### What does it return?

It returns count, tweet, replies, results, complete, tweet_id.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_tweet
