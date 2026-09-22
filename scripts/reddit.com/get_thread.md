# Get Reddit thread

Automatically get Reddit thread on reddit.com. Fetch a full Reddit thread from its URL. Returns title, op_text, score, num_comments, and comments (author, body, score, nesting depth). Compare num_comments to total_comments to detect truncation; use all_comments to expand every "more replies" thread automatically.

- Site: reddit.com
- Address: `reduck/reddit.com/get_thread`
- Updated: 2026-09-03 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_thread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_thread
```

## Input

- `id` (string, optional): Post base36 id from the permalink (e.g. "1ldvy4n"), the part after /comments/. Pass this OR url.
- `url` (string, optional): Thread URL (full https://www.reddit.com/r/.../comments/... or the /r/.../comments/... path). Pass this OR id.
- `sort` (string, optional): Comment sort via Reddit's ?sort= ("confidence" = Best). Default: Reddit's Best.
- `all_comments` (boolean, optional): Expand every "more replies" loader for the full tree (slower on big threads). Default: only comments rendered on load.

## Output

- `id` (string, required): Reddit fullname, e.g. t3_1ldvy4n
- `score` (number, required)
- `title` (string, required)
- `author` (string, required)
- `created` (string, required)
- `op_text` (string, required)
- `comments` (array, required)
- `permalink` (string, required)
- `post_type` (string, required)
- `subreddit` (string, required)
- `num_comments` (number, required): Reddit's total comment count; compare with comments.length to detect on-load truncation
- `domain` (string | null, optional)
- `content_href` (string | null, optional): Submission target: external link for link posts, the thread url for self posts
- `upvote_ratio` (number | null, optional)

## FAQ

### What does "Get Reddit thread" do?

Fetch a full Reddit thread from its URL. Returns title, op_text, score, num_comments, and comments (author, body, score, nesting depth). Compare num_comments to total_comments to detect truncation; use all_comments to expand every "more replies" thread automatically.

### How do I automatically get Reddit thread on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_thread

### Is there a reddit.com API to get Reddit thread?

You do not need one. "Get Reddit thread" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Optional: id, url, sort, all_comments.

### What does it return?

It returns id, score, title, author, domain, created, op_text, comments, permalink, post_type, subreddit, content_href, num_comments, upvote_ratio.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_thread

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_thread
