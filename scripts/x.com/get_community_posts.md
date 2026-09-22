# Get Community Posts

Automatically get Community Posts on x.com. Reads the post feed of an X Community (Top or Latest), including author, text, media, and engagement counts.

- Site: x.com
- Address: `reduck/x.com/get_community_posts`
- Updated: 2026-09-08 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_community_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_community_posts
```

## Input

- `communityId` (string, required): The community's numeric id, from its URL: x.com/i/communities/<communityId>. Found via More → Communities → a topic pill (e.g. Technology), or on any post's community badge link.
- `sort` (string, optional): Which of the community's own tabs to read. "top" is the community's default ranked view; "latest" is strict reverse-chronological.
- `limit` (integer, optional): Maximum posts to return. The tab loads a batch at a time; asking for more scrolls until the count is met or the tab stops returning new posts.

## Output

- `sort` (string, required)
- `count` (integer, required)
- `posts` (array, required)
- `community_id` (string, required)

## FAQ

### What does "Get Community Posts" do?

Reads the post feed of an X Community (Top or Latest), including author, text, media, and engagement counts.

### How do I automatically get Community Posts on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_community_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_community_posts

### Is there a x.com API to get Community Posts?

You do not need one. "Get Community Posts" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: communityId. Optional: sort, limit.

### What does it return?

It returns sort, count, posts, community_id.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_community_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_community_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_community_posts
