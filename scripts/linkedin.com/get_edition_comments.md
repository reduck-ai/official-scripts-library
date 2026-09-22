# Get LinkedIn newsletter edition comments

Automatically get LinkedIn newsletter edition comments on linkedin.com. Get the comments of a LinkedIn newsletter edition by permalink, loading up to maxComments top-level threads and each commenter's profile. Returns total and comments (urn, name, headline, profileUrl, postedAgo, text, reactions, nested replies, hasMoreReplies). The default 'relevant' sort hides low-engagement comments - use 'recent' to reach every comment; older replies behind 'See previous replies' stay unloaded (flagged by hasMoreReplies).

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_edition_comments`
- Updated: 2026-09-08 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_edition_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_edition_comments
```

## Input

- `editionUrl` (string, required): LinkedIn newsletter edition permalink, e.g. https://www.linkedin.com/pulse/<slug>-<code>/. Query string is stripped.
- `sort` (string, optional): Comment sort, mirroring the edition's own dropdown. 'relevant' is LinkedIn's default but returns a relevance-filtered subset (low-engagement comments are hidden); 'recent' shows all comments newest-first and is the only way to reach every comment.
- `maxComments` (integer, optional): Maximum top-level comment threads to return. The script wheel-scrolls until this many are loaded or the edition has no more; higher values cost proportionally more time.

## Output

- `total` (number, required): Edition-level comment count (includes replies). 0 when the social bar shows none.
- `comments` (array, required)

## FAQ

### What does "Get LinkedIn newsletter edition comments" do?

Get the comments of a LinkedIn newsletter edition by permalink, loading up to maxComments top-level threads and each commenter's profile. Returns total and comments (urn, name, headline, profileUrl, postedAgo, text, reactions, nested replies, hasMoreReplies). The default 'relevant' sort hides low-engagement comments - use 'recent' to reach every comment; older replies behind 'See previous replies' stay unloaded (flagged by hasMoreReplies).

### How do I automatically get LinkedIn newsletter edition comments on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_edition_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_edition_comments

### Is there a linkedin.com API to get LinkedIn newsletter edition comments?

You do not need one. "Get LinkedIn newsletter edition comments" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: editionUrl. Optional: sort, maxComments.

### What does it return?

It returns total, comments.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_edition_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_edition_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_edition_comments
