# Get LinkedIn post comments

Automatically get LinkedIn post comments on linkedin.com. Get the comments of a LinkedIn post by permalink, loading up to maxComments top-level threads. Returns total and comments (urn, name, headline, profileUrl, postedAgo, text, reactions, nested replies, hasMoreReplies). The default 'relevant' sort hides low-engagement comments - use 'recent' to reach every comment; older replies behind 'See previous replies' stay unloaded (flagged by hasMoreReplies).

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_post_comments`
- Updated: 2026-09-03 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_post_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post_comments
```

## Input

- `postUrl` (string, required): LinkedIn post permalink, e.g. https://www.linkedin.com/posts/<slug>-<id>-<code>/ or https://www.linkedin.com/feed/update/urn:li:activity:<id>/. Query string is stripped.
- `sort` (string, optional): Comment sort, mirroring the post's own dropdown. 'relevant' is LinkedIn's default but returns a relevance-filtered subset (low-engagement comments are hidden); 'recent' shows all comments newest-first and is the only way to reach every comment. Use 'recent' when completeness matters.
- `maxComments` (integer, optional): Maximum top-level comment threads to return. The script wheel-scrolls until this many are loaded or the post has no more; higher values cost proportionally more time.

## Output

- `total` (number, required): Post-level comment count (includes replies). 0 when the social bar shows none.
- `comments` (array, required): Top-level comments in rendered order, each with its loaded replies and a hasMoreReplies flag.

## FAQ

### What does "Get LinkedIn post comments" do?

Get the comments of a LinkedIn post by permalink, loading up to maxComments top-level threads. Returns total and comments (urn, name, headline, profileUrl, postedAgo, text, reactions, nested replies, hasMoreReplies). The default 'relevant' sort hides low-engagement comments - use 'recent' to reach every comment; older replies behind 'See previous replies' stay unloaded (flagged by hasMoreReplies).

### How do I automatically get LinkedIn post comments on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post_comments

### Is there a linkedin.com API to get LinkedIn post comments?

You do not need one. "Get LinkedIn post comments" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl. Optional: sort, maxComments.

### What does it return?

It returns total, comments.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_post_comments
