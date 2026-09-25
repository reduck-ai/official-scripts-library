# Get X user reposts

Automatically get X user reposts on x.com. Get a user's Reposts tab by handle (x.com/<handle>/reposts), the posts they reposted, newest first. It is the third profile tab, next to get_user_posts (Posts) and get_user_replies (Replies). Returns per repost: id (the repost's own id, not the original), url (the original tweet), reposted_at, and retweeted_tweet with id, url, text, created_at, lang, author {id, handle, name}, likes, retweets, replies, quotes, views, bookmarks, is_quote. How many come back depends on how far X lets the timeline scroll before throttling.

- Site: x.com
- Address: `reduck/x.com/get_user_reposts`
- Updated: 2026-09-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_user_reposts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_reposts
```

## Input

- `handle` (string, required): X handle without the @, e.g. ReduckAI
- `count` (integer, optional): Max reposts to collect, most recent first.

## FAQ

### What does "Get X user reposts" do?

Get a user's Reposts tab by handle (x.com/<handle>/reposts), the posts they reposted, newest first. It is the third profile tab, next to get_user_posts (Posts) and get_user_replies (Replies). Returns per repost: id (the repost's own id, not the original), url (the original tweet), reposted_at, and retweeted_tweet with id, url, text, created_at, lang, author {id, handle, name}, likes, retweets, replies, quotes, views, bookmarks, is_quote. How many come back depends on how far X lets the timeline scroll before throttling.

### How do I automatically get X user reposts on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_reposts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_reposts

### Is there a x.com API to get X user reposts?

You do not need one. "Get X user reposts" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle. Optional: count.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_reposts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_reposts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_user_reposts
