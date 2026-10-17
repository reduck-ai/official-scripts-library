# Get Reddit thread

Automatically get Reddit thread on reddit.com. Fetch a Reddit thread by its id or URL: the post (title, text, author, score, upvote ratio, comment count, type, link) and its comments in thread order, each with author, text, score, date, permalink and nesting depth. Needs a browser signed in to Reddit. By default it returns the first page of comments Reddit shows when the thread opens; set all_comments to expand every "more replies" and get the whole tree. num_comments counts deleted and removed comments too, so the list can be shorter than that number even when it is complete. sort picks Reddit's own comment order (best, top, new, controversial, old, Q&A).

- Site: reddit.com
- Address: `reduck/reddit.com/get_thread`
- Updated: 2026-10-16 (v17)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_thread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_thread
```

## Input

- `id` (string, optional): Post base36 id from the permalink (e.g. "1ldvy4n"), the part after /comments/. Pass this OR url.
- `url` (string, optional): Thread URL (full https://www.reddit.com/r/.../comments/... or the /r/.../comments/... path). Pass this OR id.
- `sort` (string, optional): Comment sort via Reddit's ?sort= ("confidence" = Best). Default: Reddit's Best. Applies to every url in batch mode.
- `urls` (array, optional): Read several threads in one run (max 20), one after another in the same tab, instead of id/url. Each item takes the same forms as url. Returns {results} with one result per url, in order, each with an `error` (null when fine). If Reddit blocks or rate-limits the browser, the remaining urls are not read and carry that error.
- `all_comments` (boolean, optional): Expand every "more replies" loader for the full tree (slower on big threads). Default: only comments rendered on load. Applies to every url in batch mode.

## Output

- `id` (string, optional): Reddit fullname, e.g. t3_1ldvy4n
- `score` (number | null, optional): Null while Reddit hides the post's score.
- `title` (string, optional)
- `author` (string, optional)
- `domain` (string | null, optional)
- `created` (string, optional)
- `op_text` (string, optional)
- `results` (array, optional): Batch mode only: one result per url, in order. Same fields as the single-thread output (null when the thread could not be read) plus error.
- `comments` (array, optional)
- `complete` (boolean, optional): True when every comment of the thread is in comments: no 'more replies' loader was left unexpanded. Pass all_comments to expand them.
- `permalink` (string, optional)
- `post_type` (string, optional)
- `subreddit` (string, optional)
- `content_href` (string | null, optional): Submission target: external link for link posts, the thread url for self posts
- `num_comments` (number, optional): Reddit's total comment count; compare with comments.length to detect on-load truncation
- `upvote_ratio` (number | null, optional)

## FAQ

### What does "Get Reddit thread" do?

Fetch a Reddit thread by its id or URL: the post (title, text, author, score, upvote ratio, comment count, type, link) and its comments in thread order, each with author, text, score, date, permalink and nesting depth. Needs a browser signed in to Reddit. By default it returns the first page of comments Reddit shows when the thread opens; set all_comments to expand every "more replies" and get the whole tree. num_comments counts deleted and removed comments too, so the list can be shorter than that number even when it is complete. sort picks Reddit's own comment order (best, top, new, controversial, old, Q&A).

### How do I automatically get Reddit thread on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_thread

### Is there a reddit.com API to get Reddit thread?

You do not need one. "Get Reddit thread" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Optional: id, url, sort, urls, all_comments.

### What does it return?

It returns id, score, title, author, domain, created, op_text, results, comments, complete, permalink, post_type, subreddit, content_href, num_comments, upvote_ratio.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_thread

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_thread
