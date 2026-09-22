# LinkedIn — List scheduled posts

Automatically list scheduled posts on linkedin.com. List the logged-in member's queued LinkedIn scheduled posts (text + scheduled date/time) from the Scheduled posts management panel. This is the only place these posts exist before they publish — get_post/get_feed_posts can't see them.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_scheduled_posts`
- Updated: 2026-09-15 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_scheduled_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_scheduled_posts
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of queued scheduled posts.
- `posts` (array, required)

## FAQ

### What does "LinkedIn — List scheduled posts" do?

List the logged-in member's queued LinkedIn scheduled posts (text + scheduled date/time) from the Scheduled posts management panel. This is the only place these posts exist before they publish — get_post/get_feed_posts can't see them.

### How do I automatically list scheduled posts on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_scheduled_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_scheduled_posts

### Is there a linkedin.com API to list scheduled posts?

You do not need one. "LinkedIn — List scheduled posts" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, posts.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_scheduled_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_scheduled_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_scheduled_posts
