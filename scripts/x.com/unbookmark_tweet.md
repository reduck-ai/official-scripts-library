# Remove a bookmark from a tweet on X (Twitter)

Automatically remove a bookmark from a tweet on X (Twitter) on x.com. Remove your bookmark from a tweet on X (Twitter), given its URL. A tweet that is not bookmarked is reported, not an error. Returns tweet_id, bookmarked, was_bookmarked, verified_on_page (the page was read again and shows no bookmark) and account_used.

- Site: x.com
- Address: `reduck/x.com/unbookmark_tweet`
- Updated: 2026-09-29 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/unbookmark_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/unbookmark_tweet
```

## Input

- `tweet_url` (string, required): Full URL of the tweet, e.g. https://x.com/handle/status/123

## Output

- `tweet_id` (string, required)
- `bookmarked` (boolean, required)
- `account_used` (string | null, required): handle of the logged-in account that performed the action, read from the page itself rather than assumed from input
- `was_bookmarked` (boolean, required): true if the tweet was bookmarked before this call
- `verified_on_page` (boolean, required): true if the page was re-inspected after the action and confirmed the tweet no longer shows as bookmarked

## FAQ

### What does "Remove a bookmark from a tweet on X (Twitter)" do?

Remove your bookmark from a tweet on X (Twitter), given its URL. A tweet that is not bookmarked is reported, not an error. Returns tweet_id, bookmarked, was_bookmarked, verified_on_page (the page was read again and shows no bookmark) and account_used.

### How do I automatically remove a bookmark from a tweet on X (Twitter) on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/unbookmark_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unbookmark_tweet

### Is there a x.com API to remove a bookmark from a tweet on X (Twitter)?

You do not need one. "Remove a bookmark from a tweet on X (Twitter)" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: tweet_url.

### What does it return?

It returns tweet_id, bookmarked, account_used, was_bookmarked, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/unbookmark_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unbookmark_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/unbookmark_tweet
