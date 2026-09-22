# Crosspost a Reddit post

Automatically crosspost a Reddit post on reddit.com. Crosspost (Reddit's "Repost") an existing post into another subreddit, keeping the link back to the original. Takes the source post URL and a target subreddit; optionally overrides the title (defaults to the source title). Returns the new crosspost's fullname (t3_), target subreddit and URL. This creates a real, public crosspost: many communities disable reposting, and the script fails loudly if the target does; some also require a flair that blocks the post. It needs a Reddit account already signed in in the browser, and runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/crosspost`
- Updated: 2026-08-20 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/crosspost`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/crosspost
```

## Input

- `subreddit` (string, required): Target community to crosspost into, with or without r/ prefix
- `source_url` (string, required): URL of the post to crosspost (any /r/<sub>/comments/<id>/... permalink)
- `title` (string, optional): Optional title override. Omit to keep the source post's title (Reddit pre-fills it, truncated to 300 chars).

## Output

- `url` (string | null, required): URL of the created crosspost, or null when already_present short-circuited before posting
- `postId` (string | null, required): Fullname of the created crosspost, or null when already_present short-circuited before posting
- `posted` (boolean, required)
- `sourceId` (string, required)
- `subreddit` (string, required)
- `account_used` (string, required)
- `already_present` (boolean, required)
- `verified_on_page` (boolean, required)

## FAQ

### What does "Crosspost a Reddit post" do?

Crosspost (Reddit's "Repost") an existing post into another subreddit, keeping the link back to the original. Takes the source post URL and a target subreddit; optionally overrides the title (defaults to the source title). Returns the new crosspost's fullname (t3_), target subreddit and URL. This creates a real, public crosspost: many communities disable reposting, and the script fails loudly if the target does; some also require a flair that blocks the post. It needs a Reddit account already signed in in the browser, and runs only via the browser extension, not the hosted cloud browser.

### How do I automatically crosspost a Reddit post on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/crosspost, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/crosspost

### Is there a reddit.com API to crosspost a Reddit post?

You do not need one. "Crosspost a Reddit post" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: source_url, subreddit. Optional: title.

### What does it return?

It returns url, postId, posted, sourceId, subreddit, account_used, already_present, verified_on_page.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/crosspost, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/crosspost

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/crosspost
