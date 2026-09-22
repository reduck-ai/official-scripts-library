# Like tweet

Automatically like tweet on x.com. Like a tweet given its URL. Safe to repeat: an already-liked tweet is reported, not re-liked. Returns tweet_id, liked, was_liked.

- Site: x.com
- Address: `reduck/x.com/like_tweet`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/like_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/like_tweet
```

## Input

- `tweet_url` (string, required): Full URL of the tweet, e.g. https://x.com/handle/status/123

## Output

- `liked` (boolean, required)
- `tweet_id` (string, required)
- `was_liked` (boolean, required): already_present signal: true if the tweet was already liked before this call
- `verified_on_page` (boolean, required): true if the page was reloaded and re-inspected after the action, confirming the like is actually visible/present
- `account_used` (string | null, optional): handle of the logged-in account that performed the action, read from the account switcher UI (not assumed from input)

## FAQ

### What does "Like tweet" do?

Like a tweet given its URL. Safe to repeat: an already-liked tweet is reported, not re-liked. Returns tweet_id, liked, was_liked.

### How do I automatically like tweet on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/like_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/like_tweet

### Is there a x.com API to like tweet?

You do not need one. "Like tweet" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: tweet_url.

### What does it return?

It returns liked, tweet_id, was_liked, account_used, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/like_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/like_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/like_tweet
