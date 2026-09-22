# Get Substack post

Automatically get Substack post on substack.com. Fetch a single Substack post by its URL: title, subtitle, author, publish date, paywall status, full HTML body (when accessible), word count, and reaction/comment/restack counts.

- Site: substack.com
- Address: `reduck/substack.com/get_post`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/substack.com/get_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/substack.com/get_post
```

## Input

- `url` (string, required): Full URL of the Substack post, e.g. https://example.substack.com/p/my-post-slug

## Output

- `url` (string, required)
- `slug` (string, required)
- `title` (string, required)
- `postId` (number, required)
- `authors` (array, required)
- `audience` (string, required)
- `hasAudio` (boolean, required)
- `hasVideo` (boolean, required)
- `postDate` (string, required)
- `postType` (string, required)
- `isPaywalled` (boolean, required)
- `canonicalUrl` (string, required)
- `bodyHtml` (string | null, optional)
- `restacks` (number | null, optional)
- `subtitle` (string | null, optional)
- `updatedAt` (string | null, optional)
- `wordcount` (number | null, optional)
- `coverImage` (string | null, optional)
- `commentCount` (number | null, optional)
- `reactionCount` (number | null, optional)
- `truncatedText` (string | null, optional)
- `mediaDurationSeconds` (number | null, optional)

## FAQ

### What does "Get Substack post" do?

Fetch a single Substack post by its URL: title, subtitle, author, publish date, paywall status, full HTML body (when accessible), word count, and reaction/comment/restack counts.

### How do I automatically get Substack post on substack.com?

Ask an AI agent connected to Reduck to run reduck/substack.com/get_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/get_post

### Is there a substack.com API to get Substack post?

You do not need one. "Get Substack post" drives the real substack.com pages in a browser, so it works whether or not substack.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, slug, title, postId, authors, audience, bodyHtml, hasAudio, hasVideo, postDate, postType, restacks, subtitle, updatedAt, wordcount, coverImage, isPaywalled, canonicalUrl, commentCount, reactionCount, truncatedText, mediaDurationSeconds.

### Do I need to be logged in to substack.com?

No. It only uses pages of substack.com that are reachable without signing in.

### Does it change anything on substack.com, or only read data?

It only reads. It looks things up on substack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/substack.com/get_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/get_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/substack.com/get_post
