# Unpin tweet from profile

Automatically unpin tweet from profile on x.com. Unpin your own tweet from the top of your profile, given its URL. Tweets that aren't currently pinned are reported rather than erroring. Returns tweet_id, pinned, was_pinned, and account_used. X can briefly serve a stale pinned-state right after a preceding pin/unpin on the account — if you just changed the pin state, allow a few seconds before calling this again for a reliable was_pinned reading.

- Site: x.com
- Address: `reduck/x.com/unpin_tweet`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/unpin_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/unpin_tweet
```

## Input

- `tweet_url` (string, required): Full URL of your tweet to unpin, e.g. https://x.com/handle/status/123.

## Output

- `pinned` (boolean, required)
- `tweet_id` (string, required)
- `was_pinned` (boolean, required): true if the tweet was pinned before this call.
- `account_used` (string | null, optional): handle of the logged-in account that performed the action, read from the account switcher UI.

## FAQ

### What does "Unpin tweet from profile" do?

Unpin your own tweet from the top of your profile, given its URL. Tweets that aren't currently pinned are reported rather than erroring. Returns tweet_id, pinned, was_pinned, and account_used. X can briefly serve a stale pinned-state right after a preceding pin/unpin on the account — if you just changed the pin state, allow a few seconds before calling this again for a reliable was_pinned reading.

### How do I automatically unpin tweet from profile on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/unpin_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unpin_tweet

### Is there a x.com API to unpin tweet from profile?

You do not need one. "Unpin tweet from profile" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: tweet_url.

### What does it return?

It returns pinned, tweet_id, was_pinned, account_used.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/unpin_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unpin_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/unpin_tweet
