# Vote on Reddit post or comment

Automatically vote on Reddit post or comment on reddit.com. Up, down, or clear your vote on a Reddit post or comment by its URL/permalink. Safe to repeat: it only changes the vote if it isn't already in the requested state. You cannot downvote or clear the vote on your own post, since Reddit forces the author's upvote and the change reverts on reload. Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/vote`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/vote`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/vote
```

## Input

- `url` (string, required): Post URL or comment permalink (relative path or full URL). A comment permalink contains /comment/<id>/.
- `direction` (string, required): Target vote state: up, down, or clear (remove vote)

## Output

- `target` (string, required): Fullname of the voted thing (t3_ post / t1_ comment)
- `changed` (boolean, required): False when already in the requested state (no click, no mutation)
- `requested` (string, required)
- `voteState` (string, required): Resulting vote state as reported by Reddit (e.g. UP/DOWN/NONE)
- `ok` (boolean, optional)

## FAQ

### What does "Vote on Reddit post or comment" do?

Up, down, or clear your vote on a Reddit post or comment by its URL/permalink. Safe to repeat: it only changes the vote if it isn't already in the requested state. You cannot downvote or clear the vote on your own post, since Reddit forces the author's upvote and the change reverts on reload. Runs only via the browser extension, not the hosted cloud browser.

### How do I automatically vote on Reddit post or comment on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/vote, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/vote

### Is there a reddit.com API to vote on Reddit post or comment?

You do not need one. "Vote on Reddit post or comment" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: url, direction.

### What does it return?

It returns ok, target, changed, requested, voteState.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/vote, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/vote

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/vote
