# Get Medium author's posts

Automatically get Medium author's posts on medium.com. List an author's published posts on Medium (from their profile Home tab): title, URL, tags, claps, read time, published date, and whether locked (member-only). No login required.

- Site: medium.com
- Address: `reduck/medium.com/get_author_posts`
- Updated: 2026-09-02 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/medium.com/get_author_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/medium.com/get_author_posts
```

## Input

- `username` (string, required): Medium username without @, e.g. "shedlesky" (from medium.com/@<username>)

## Output

- `posts` (array, required)
- `username` (string, required)
- `available` (boolean, required)

## FAQ

### What does "Get Medium author's posts" do?

List an author's published posts on Medium (from their profile Home tab): title, URL, tags, claps, read time, published date, and whether locked (member-only). No login required.

### How do I automatically get Medium author's posts on medium.com?

Ask an AI agent connected to Reduck to run reduck/medium.com/get_author_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/medium.com/get_author_posts

### Is there a medium.com API to get Medium author's posts?

You do not need one. "Get Medium author's posts" drives the real medium.com pages in a browser, so it works whether or not medium.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns posts, username, available.

### Do I need to be logged in to medium.com?

No. It only uses pages of medium.com that are reachable without signing in.

### Does it change anything on medium.com, or only read data?

It only reads. It looks things up on medium.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/medium.com/get_author_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/medium.com/get_author_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/medium.com/get_author_posts
