# Like a Threads post

Automatically like a Threads post on threads.com. Like a post on Threads by its URL, as the signed-in account. Reports whether the post was already liked so a repeat run does not double-count.

- Site: threads.com
- Address: `reduck/threads.com/like_post`
- Updated: 2026-09-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/threads.com/like_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/threads.com/like_post
```

## Input

- `postUrl` (string, required): Full URL of the Threads post, e.g. https://www.threads.com/@zuck/post/ABC123.

## Output

- `code` (string, required): The post's short code, parsed from the URL.
- `liked` (boolean, required): True when the post is liked by the signed-in account after this run.
- `postUrl` (string, required): The post URL that was acted on.
- `alreadyLiked` (boolean, required): True when the post was already liked before this run, in which case nothing was clicked and the like was left untouched.
- `likeCount` (string | null, optional): The like count as the post displays it after the run, verbatim (e.g. "1.7K"). Threads abbreviates large counts, so this is a display string, not a number.

## FAQ

### What does "Like a Threads post" do?

Like a post on Threads by its URL, as the signed-in account. Reports whether the post was already liked so a repeat run does not double-count.

### How do I automatically like a Threads post on threads.com?

Ask an AI agent connected to Reduck to run reduck/threads.com/like_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/like_post

### Is there a threads.com API to like a Threads post?

You do not need one. "Like a Threads post" drives the real threads.com pages in a browser, so it works whether or not threads.com offers an API for this.

### What information do I need to provide?

Required: postUrl.

### What does it return?

It returns code, liked, postUrl, likeCount, alreadyLiked.

### Do I need to be logged in to threads.com?

Yes. It acts as you on threads.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the threads.com cookies saved by the Reduck extension.

### Does it change anything on threads.com, or only read data?

It makes changes on threads.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/threads.com/like_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/like_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/threads.com/like_post
