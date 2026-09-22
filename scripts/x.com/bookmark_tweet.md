# Bookmark tweet

Automatically bookmark tweet on x.com. Bookmark a tweet given its URL. Already-bookmarked tweets are reported rather than re-bookmarked. Returns tweet_id, bookmarked, was_bookmarked.

- Site: x.com
- Address: `reduck/x.com/bookmark_tweet`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/bookmark_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/bookmark_tweet
```

## Input

- `tweet_url` (string, required): Full URL of the tweet, e.g. https://x.com/handle/status/123

## Output

- `tweet_id` (string, required)
- `bookmarked` (boolean, required)
- `was_bookmarked` (boolean, required): true if already bookmarked before this call

## FAQ

### What does "Bookmark tweet" do?

Bookmark a tweet given its URL. Already-bookmarked tweets are reported rather than re-bookmarked. Returns tweet_id, bookmarked, was_bookmarked.

### How do I automatically bookmark tweet on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/bookmark_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/bookmark_tweet

### Is there a x.com API to bookmark tweet?

You do not need one. "Bookmark tweet" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: tweet_url.

### What does it return?

It returns tweet_id, bookmarked, was_bookmarked.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/bookmark_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/bookmark_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/bookmark_tweet
