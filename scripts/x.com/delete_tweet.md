# Delete tweet

Automatically delete tweet on x.com. Delete one of your own tweets given its URL. Returns the deleted tweet id and a deleted flag.

- Site: x.com
- Address: `reduck/x.com/delete_tweet`
- Updated: 2026-08-26 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/delete_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/delete_tweet
```

## Input

- `tweet_url` (string, required): Full URL of your tweet to delete, e.g. https://x.com/handle/status/123. This deletes immediately and cannot be undone, and the script has no preview or confirmation step of its own. Before calling it, show the exact tweet URL and its content to the person you are helping and get their explicit approval for that specific tweet; do not infer approval from an earlier or unrelated message.

## Output

- `deleted` (boolean, required)
- `tweet_id` (string, required)
- `verified_on_page` (boolean, required): true if the page was reloaded after deletion and the tweet is confirmed gone (article removed or a deleted/tombstone message shown)
- `account_used` (string | null, optional): handle of the logged-in account that performed the action, read from the account switcher UI (not assumed from input)

## FAQ

### What does "Delete tweet" do?

Delete one of your own tweets given its URL. Returns the deleted tweet id and a deleted flag.

### How do I automatically delete tweet on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/delete_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/delete_tweet

### Is there a x.com API to delete tweet?

You do not need one. "Delete tweet" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: tweet_url.

### What does it return?

It returns deleted, tweet_id, account_used, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/delete_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/delete_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/delete_tweet
