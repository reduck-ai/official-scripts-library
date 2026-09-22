# Search Threads posts

Automatically search Threads posts on threads.com. Search Threads for posts matching a keyword, hashtag, or topic and return the matching posts with author, text, and engagement counts.

- Site: threads.com
- Address: `reduck/threads.com/search_posts`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/threads.com/search_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/threads.com/search_posts
```

## Input

- `query` (string, required): Search text (keyword, hashtag, or topic) to look up on Threads

## Output

- `posts` (array, required)
- `query` (string, required)

## FAQ

### What does "Search Threads posts" do?

Search Threads for posts matching a keyword, hashtag, or topic and return the matching posts with author, text, and engagement counts.

### How do I automatically search Threads posts on threads.com?

Ask an AI agent connected to Reduck to run reduck/threads.com/search_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/search_posts

### Is there a threads.com API to search Threads posts?

You do not need one. "Search Threads posts" drives the real threads.com pages in a browser, so it works whether or not threads.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns posts, query.

### Do I need to be logged in to threads.com?

No. It only uses pages of threads.com that are reachable without signing in.

### Does it change anything on threads.com, or only read data?

It only reads. It looks things up on threads.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/threads.com/search_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/search_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/threads.com/search_posts
