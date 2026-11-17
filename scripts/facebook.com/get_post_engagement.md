# Get the comments and reactions of a Facebook post

Automatically get the comments and reactions of a Facebook post on facebook.com. Get the engagement of a Facebook post from its link: total reactions, the count per reaction type, the number of comments and shares, and the comments themselves with author, text, reactions and whether each is a reply. Comments come in the order Facebook shows them (most relevant first) and are capped by commentLimit. For a reel, only the counts are returned. A post that is deleted, private or not visible to the browser returns a clear error.

- Site: facebook.com
- Address: `reduck/facebook.com/get_post_engagement`
- Updated: 2026-11-16 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/get_post_engagement`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_post_engagement
```

## Input

- `postUrl` (string, required): Link to the post, photo, video or reel.
- `commentLimit` (integer, optional): How many comments to return at most.

## Output

- `post` (object, required)
- `comments` (array, required)
- `isReel` (boolean, optional): Present and true when the link is a reel: counts only, no comments.
- `reelId` (string, optional): The reel's id, when the link is a reel.

## FAQ

### What does "Get the comments and reactions of a Facebook post" do?

Get the engagement of a Facebook post from its link: total reactions, the count per reaction type, the number of comments and shares, and the comments themselves with author, text, reactions and whether each is a reply. Comments come in the order Facebook shows them (most relevant first) and are capped by commentLimit. For a reel, only the counts are returned. A post that is deleted, private or not visible to the browser returns a clear error.

### How do I automatically get the comments and reactions of a Facebook post on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_post_engagement, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_post_engagement

### Is there a facebook.com API to get the comments and reactions of a Facebook post?

You do not need one. "Get the comments and reactions of a Facebook post" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: postUrl. Optional: commentLimit.

### What does it return?

It returns post, isReel, reelId, comments.

### Do I need to be logged in to facebook.com?

No. It only uses pages of facebook.com that are reachable without signing in.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_post_engagement, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_post_engagement

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/get_post_engagement
