# Get Instagram home feed

Automatically get Instagram home feed on instagram.com. Fetch the posts from your Instagram home (For You) feed.

- Site: instagram.com
- Address: `reduck/instagram.com/get_feed`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_feed`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_feed
```

## Input

- `count` (integer, optional): Number of home-feed posts to return (scrolls to load more). Default 12.

## Output

- `posts` (array, required)

## FAQ

### What does "Get Instagram home feed" do?

Fetch the posts from your Instagram home (For You) feed.

### How do I automatically get Instagram home feed on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_feed, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_feed

### Is there a instagram.com API to get Instagram home feed?

You do not need one. "Get Instagram home feed" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns posts.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

Unknown: its author has not declared whether it changes anything on instagram.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_feed, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_feed

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_feed
