# Submit Reddit post

Automatically submit Reddit post on reddit.com. Create a text post (thread) in a subreddit. Returns the new post's ID, subreddit and URL. Posts a real thread under the logged-in account; text posts only (no link/image); some subreddits require a flair and will block the post. Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/submit_post`
- Updated: 2026-09-10 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/submit_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/submit_post
```

## Input

- `body` (string, required): Post body text (plain text / markdown). Supports inline @-mentions (u/name — Reddit auto-links them) and links; inline images/banners are not supported (would require a file upload, CLI-only).
- `title` (string, required): Post title
- `subreddit` (string, required): Target subreddit, with or without r/ prefix. Must be a subreddit that does NOT require a post flair: this script cannot set one, so a flair-required subreddit is refused up front, before anything is posted, with the list of flairs that subreddit offers.

## Output

- `url` (string, required)
- `postId` (string, required): Fullname of the created post, e.g. t3_xxxxx
- `posted` (boolean, required)
- `subreddit` (string, required)
- `account_used` (string, required): The real logged-in Reddit handle that performed the action, read from the page's own account drawer (not assumed from args)
- `already_present` (boolean, required): Whether an identical-title post by this account already existed in the subreddit before publishing (checked via the account's own submitted-posts list)
- `verified_on_page` (boolean, required): Whether the script reloaded the created post's own page afterward and confirmed it's actually visible there with the right title and author

## FAQ

### What does "Submit Reddit post" do?

Create a text post (thread) in a subreddit. Returns the new post's ID, subreddit and URL. Posts a real thread under the logged-in account; text posts only (no link/image); some subreddits require a flair and will block the post. Runs only via the browser extension, not the hosted cloud browser.

### How do I automatically submit Reddit post on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/submit_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/submit_post

### Is there a reddit.com API to submit Reddit post?

You do not need one. "Submit Reddit post" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: subreddit, title, body.

### What does it return?

It returns url, postId, posted, subreddit, account_used, already_present, verified_on_page.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/submit_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/submit_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/submit_post
