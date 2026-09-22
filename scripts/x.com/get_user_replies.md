# Get X user replies

Automatically get X user replies on x.com. Get a user's Replies tab by handle (x.com/<handle>/with_replies) — their replies, newest first, plus the user's own tweets that sit at the root of those reply threads (self-threads). Standalone posts and reposts are not on this tab: use get_user_posts for the Posts tab, and X keeps reposts on a separate Reposts tab. Owner-authored rows only — the thread-context tweets X shows from other accounts are excluded. Returns per tweet: id, url, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote, plus in_reply_to {id, author_handle} (null on a plain post) so replies are distinguishable and the parent is fetchable via get_tweet. Count is capped by how far X paginates before throttling.

- Site: x.com
- Address: `reduck/x.com/get_user_replies`
- Updated: 2026-09-03 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_user_replies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_replies
```

## Input

- `handle` (string, required): X handle without the @, e.g. BernieSanders
- `count` (integer, optional): Max rows to collect. Capped by how far X's timeline paginates before throttling.

## FAQ

### What does "Get X user replies" do?

Get a user's Replies tab by handle (x.com/<handle>/with_replies) — their replies, newest first, plus the user's own tweets that sit at the root of those reply threads (self-threads). Standalone posts and reposts are not on this tab: use get_user_posts for the Posts tab, and X keeps reposts on a separate Reposts tab. Owner-authored rows only — the thread-context tweets X shows from other accounts are excluded. Returns per tweet: id, url, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote, plus in_reply_to {id, author_handle} (null on a plain post) so replies are distinguishable and the parent is fetchable via get_tweet. Count is capped by how far X paginates before throttling.

### How do I automatically get X user replies on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_replies

### Is there a x.com API to get X user replies?

You do not need one. "Get X user replies" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle. Optional: count.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_replies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_user_replies
