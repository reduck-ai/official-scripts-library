# Leave subreddit

Automatically leave subreddit on reddit.com. Leave (unsubscribe from) a subreddit by name. If you're not a member, nothing changes and changed is returned as false. Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/leave_subreddit`
- Updated: 2026-07-31 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/leave_subreddit`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/leave_subreddit
```

## Input

- `subreddit` (string, required): Subreddit name, with or without r/ prefix

## Output

- `joined` (boolean, required)
- `changed` (boolean, required): False when not a member (no click, no mutation)
- `subreddit` (string, required)

## FAQ

### What does "Leave subreddit" do?

Leave (unsubscribe from) a subreddit by name. If you're not a member, nothing changes and changed is returned as false. Runs only via the browser extension, not the hosted cloud browser.

### How do I automatically leave subreddit on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/leave_subreddit, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/leave_subreddit

### Is there a reddit.com API to leave subreddit?

You do not need one. "Leave subreddit" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: subreddit.

### What does it return?

It returns joined, changed, subreddit.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/leave_subreddit, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/leave_subreddit

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/leave_subreddit
