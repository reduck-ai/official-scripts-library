# List Substack newsletter posts

Automatically list Substack newsletter posts on substack.com. List a Substack publication's posts from its archive, newest or top first, with optional keyword search and pagination. Returns each post's title, slug, publish date, paywall status, and reaction/comment/restack counts.

- Site: substack.com
- Address: `reduck/substack.com/list_newsletter_posts`
- Updated: 2026-08-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/substack.com/list_newsletter_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/substack.com/list_newsletter_posts
```

## Input

- `publicationUrl` (string, required): Base URL of the Substack publication, e.g. https://example.substack.com (a publication's own domain also works)
- `sort` (string, optional): Sort order: "new" (most recent first) or "top" (most reactions first)
- `limit` (number, optional): Maximum number of posts to return
- `offset` (number, optional): Number of posts to skip, for pagination
- `search` (string, optional): Optional keyword filter over the publication's posts

## Output

- `sort` (string, required)
- `count` (number, required)
- `limit` (number, required)
- `posts` (array, required)
- `offset` (number, required)
- `publicationUrl` (string, required)

## FAQ

### What does "List Substack newsletter posts" do?

List a Substack publication's posts from its archive, newest or top first, with optional keyword search and pagination. Returns each post's title, slug, publish date, paywall status, and reaction/comment/restack counts.

### How do I automatically list Substack newsletter posts on substack.com?

Ask an AI agent connected to Reduck to run reduck/substack.com/list_newsletter_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/list_newsletter_posts

### Is there a substack.com API to list Substack newsletter posts?

You do not need one. "List Substack newsletter posts" drives the real substack.com pages in a browser, so it works whether or not substack.com offers an API for this.

### What information do I need to provide?

Required: publicationUrl. Optional: sort, limit, offset, search.

### What does it return?

It returns sort, count, limit, posts, offset, publicationUrl.

### Do I need to be logged in to substack.com?

No. It only uses pages of substack.com that are reachable without signing in.

### Does it change anything on substack.com, or only read data?

It only reads. It looks things up on substack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/substack.com/list_newsletter_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/list_newsletter_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/substack.com/list_newsletter_posts
