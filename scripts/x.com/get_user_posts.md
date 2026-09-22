# Get X user posts

Automatically get X user posts on x.com. Get a user's Posts tab by handle (x.com/<handle>) — their own tweets and self-threads, newest first. Excludes replies to others (see get_user_replies for the Replies tab), and excludes reposts, which X keeps on a separate Reposts tab. The post count shown on the profile header includes replies, so expect fewer items than that number. Returns per tweet: id, url, text, created_at, lang, likes, retweets, replies, quotes, views, bookmarks, is_retweet, is_quote. Count is capped by how far X paginates before throttling.

- Site: x.com
- Address: `reduck/x.com/get_user_posts`
- Updated: 2026-09-03 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_user_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_posts
```

## Input

- `handle` (string, required): X handle without the @, e.g. BernieSanders
- `count` (integer, optional): Max tweets to collect. Capped by how far X's timeline paginates before throttling.

## FAQ

### What does "Get X user posts" do?

Get a user's Posts tab by handle (x.com/<handle>) — their own tweets and self-threads, newest first. Excludes replies to others (see get_user_replies for the Replies tab), and excludes reposts, which X keeps on a separate Reposts tab. The post count shown on the profile header includes replies, so expect fewer items than that number. Returns per tweet: id, url, text, created_at, lang, likes, retweets, replies, quotes, views, bookmarks, is_retweet, is_quote. Count is capped by how far X paginates before throttling.

### How do I automatically get X user posts on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_posts

### Is there a x.com API to get X user posts?

You do not need one. "Get X user posts" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle. Optional: count.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_user_posts
