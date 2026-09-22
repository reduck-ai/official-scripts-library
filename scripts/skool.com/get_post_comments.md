# Get comments on a Skool post

Automatically get comments on a Skool post on skool.com. Read the comments on a Skool community post, addressed by the post's URL. Returns each comment with its author name and handle, profile link, text, time, upvote count, and how it sits in the thread — whether it is a reply and which comment it answers — plus a flag marking the comments written by the signed-in account. Replies are included and keep their position under the comment they answer. Reports the post's own comment total alongside the number returned, and says plainly when a thread is too large to return in full rather than trimming it silently.

- Site: skool.com
- Address: `reduck/skool.com/get_post_comments`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/skool.com/get_post_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/skool.com/get_post_comments
```

## Input

- `postUrl` (string, required): Full URL of the Skool post, e.g. https://www.skool.com/<community>/<post-slug>. The community part is case-insensitive.
- `limit` (integer, optional): How many top-level comments to return. Values above 25 also pull the oldest window, since the site serves comments in a newest and an oldest window rather than continuous pages.

## Output

- `count` (integer, required): Number of comments actually returned, replies included.
- `postId` (string, required)
- `postUrl` (string, required)
- `comments` (array, required)
- `complete` (boolean, required): True when every comment on the post was returned. False when the thread is larger than the site will serve in one read.
- `group` (string | null, optional)
- `postTitle` (string | null, optional)
- `accountUsed` (string | null, optional): Handle of the signed-in account, read from the session rather than assumed.
- `totalOnPost` (integer | null, optional): Comment total the post itself reports, replies included, independent of limit.

## FAQ

### What does "Get comments on a Skool post" do?

Read the comments on a Skool community post, addressed by the post's URL. Returns each comment with its author name and handle, profile link, text, time, upvote count, and how it sits in the thread — whether it is a reply and which comment it answers — plus a flag marking the comments written by the signed-in account. Replies are included and keep their position under the comment they answer. Reports the post's own comment total alongside the number returned, and says plainly when a thread is too large to return in full rather than trimming it silently.

### How do I automatically get comments on a Skool post on skool.com?

Ask an AI agent connected to Reduck to run reduck/skool.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/get_post_comments

### Is there a skool.com API to get comments on a Skool post?

You do not need one. "Get comments on a Skool post" drives the real skool.com pages in a browser, so it works whether or not skool.com offers an API for this.

### What information do I need to provide?

Required: postUrl. Optional: limit.

### What does it return?

It returns count, group, postId, postUrl, comments, complete, postTitle, accountUsed, totalOnPost.

### Do I need to be logged in to skool.com?

Yes. It acts as you on skool.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the skool.com cookies saved by the Reduck extension.

### Does it change anything on skool.com, or only read data?

It only reads. It looks things up on skool.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/skool.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/get_post_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/skool.com/get_post_comments
