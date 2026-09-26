# Get the comments and reactions of a Facebook post

Automatically get the comments and reactions of a Facebook post on facebook.com. Get the comments and reactions of a Facebook post as structured data, with the reaction breakdown by type. Get reactions (total + breakdown by type), comment and share counts, and loaded comments (author, text, reactions, reply flag) for a Facebook post URL. Comments are an infinite-scroll sample in non-deterministic "Most relevant" order, capped by commentLimit.

- Site: facebook.com
- Address: `reduck/facebook.com/get_post_engagement`
- Updated: 2026-09-25 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/get_post_engagement`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_post_engagement
```

## Input

- `postUrl` (string, required)

## Output

- `post` (object, optional)
- `comments` (array, optional)

## FAQ

### What does "Get the comments and reactions of a Facebook post" do?

Get the comments and reactions of a Facebook post as structured data, with the reaction breakdown by type. Get reactions (total + breakdown by type), comment and share counts, and loaded comments (author, text, reactions, reply flag) for a Facebook post URL. Comments are an infinite-scroll sample in non-deterministic "Most relevant" order, capped by commentLimit.

### How do I automatically get the comments and reactions of a Facebook post on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_post_engagement, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_post_engagement

### Is there a facebook.com API to get the comments and reactions of a Facebook post?

You do not need one. "Get the comments and reactions of a Facebook post" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: postUrl.

### What does it return?

It returns post, comments.

### Do I need to be logged in to facebook.com?

No. It only uses pages of facebook.com that are reachable without signing in.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_post_engagement, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_post_engagement

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/get_post_engagement
