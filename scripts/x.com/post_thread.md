# Post X tweet thread

Automatically post X tweet thread on x.com. Post a thread (tweetstorm) of N linked tweets in one go via the native multi-post composer. Returns the posted tweets in order with their ids/urls and the thread's root url.

- Site: x.com
- Address: `reduck/x.com/post_thread`
- Updated: 2026-08-26 (v18)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/post_thread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/post_thread
```

## Input

- `tweets` (array, required): Ordered tweet texts; each ≤280 chars. tweets[0] is the root, the rest are chained replies. Any @handle in the text is validated against a real, non-suspended X account before anything is posted — the run throws naming the bad handle if one doesn't resolve. Every call posts immediately and irreversibly, with no preview or confirmation step inside the script, so show the exact text to the user and get their explicit approval for this specific content before running — approval from an earlier or unrelated message does not carry over.

## Output

- `count` (integer, required)
- `tweets` (array, required)
- `thread_url` (string, required): URL of the root tweet.
- `account_used` (string, required): Real handle that posted the thread, echoed from the CreateTweet response (not assumed from input).
- `already_present` (boolean, required): Whether the root tweet's exact text already existed on the account's Posts tab before this run attempted to publish.
- `verified_on_page` (boolean, required): Whether every posted tweet was confirmed rendered at its own permalink after publishing. Each tweet id is checked on its own page rather than by re-reading the thread root, because the root's conversation timeline is virtualized and renders the chained replies progressively.

## FAQ

### What does "Post X tweet thread" do?

Post a thread (tweetstorm) of N linked tweets in one go via the native multi-post composer. Returns the posted tweets in order with their ids/urls and the thread's root url.

### How do I automatically post X tweet thread on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/post_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/post_thread

### Is there a x.com API to post X tweet thread?

You do not need one. "Post X tweet thread" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: tweets.

### What does it return?

It returns count, tweets, thread_url, account_used, already_present, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/post_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/post_thread

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/post_thread
