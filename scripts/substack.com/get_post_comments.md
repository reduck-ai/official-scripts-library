# Get Substack post comments

Automatically get Substack post comments on substack.com. Get the comments on a Substack post by its URL, including nested replies. Supports sorting by top reactions or newest first. Returns each comment's author, text, date, reaction count, and reply thread.

- Site: substack.com
- Address: `reduck/substack.com/get_post_comments`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/substack.com/get_post_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/substack.com/get_post_comments
```

## Input

- `url` (string, required): Full URL of the Substack post, e.g. https://example.substack.com/p/my-post-slug
- `sort` (string, optional): Comment sort order: "top" (most reactions first) or "newest" (most recent first)

## Output

- `url` (string, required)
- `sort` (string, required)
- `postId` (number, required)
- `audience` (string, required)
- `comments` (array, required)
- `isPaywalled` (boolean, required)
- `totalComments` (number | null, optional)

## FAQ

### What does "Get Substack post comments" do?

Get the comments on a Substack post by its URL, including nested replies. Supports sorting by top reactions or newest first. Returns each comment's author, text, date, reaction count, and reply thread.

### How do I automatically get Substack post comments on substack.com?

Ask an AI agent connected to Reduck to run reduck/substack.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/get_post_comments

### Is there a substack.com API to get Substack post comments?

You do not need one. "Get Substack post comments" drives the real substack.com pages in a browser, so it works whether or not substack.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: sort.

### What does it return?

It returns url, sort, postId, audience, comments, isPaywalled, totalComments.

### Do I need to be logged in to substack.com?

No. It only uses pages of substack.com that are reachable without signing in.

### Does it change anything on substack.com, or only read data?

It only reads. It looks things up on substack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/substack.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/get_post_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/substack.com/get_post_comments
