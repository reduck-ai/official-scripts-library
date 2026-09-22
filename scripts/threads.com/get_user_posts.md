# Get Threads user posts

Automatically get Threads user posts on threads.com. Fetch the posts on a Threads user's profile timeline, with text and engagement counts.

- Site: threads.com
- Address: `reduck/threads.com/get_user_posts`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/threads.com/get_user_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/threads.com/get_user_posts
```

## Input

- `username` (string, required): Threads username, with or without the leading @

## Output

- `found` (boolean, required): false if the username doesn't resolve to a viewable profile
- `posts` (array, required)
- `username` (string, required)

## FAQ

### What does "Get Threads user posts" do?

Fetch the posts on a Threads user's profile timeline, with text and engagement counts.

### How do I automatically get Threads user posts on threads.com?

Ask an AI agent connected to Reduck to run reduck/threads.com/get_user_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/get_user_posts

### Is there a threads.com API to get Threads user posts?

You do not need one. "Get Threads user posts" drives the real threads.com pages in a browser, so it works whether or not threads.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns found, posts, username.

### Do I need to be logged in to threads.com?

No. It only uses pages of threads.com that are reachable without signing in.

### Does it change anything on threads.com, or only read data?

It only reads. It looks things up on threads.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/threads.com/get_user_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/get_user_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/threads.com/get_user_posts
