# LinkedIn — Cancel scheduled post

Automatically cancel scheduled post on linkedin.com. Cancel one of the logged-in member's queued LinkedIn scheduled posts by its exact body text, via the Scheduled posts management panel. delete_post can't reach these — a scheduled post has no permalink until it actually publishes.

- Site: linkedin.com
- Address: `reduck/linkedin.com/remove_scheduled_post`
- Updated: 2026-09-08 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/remove_scheduled_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/remove_scheduled_post
```

## Input

- `text` (string, required): The exact body text of the queued scheduled post to cancel (from create_post's scheduledFor / get_scheduled_posts' text). If more than one queued post shares this exact text, the run refuses to guess and throws.

## Output

- `text` (string, required): Echoes the input text.
- `found` (boolean, required): True if a queued scheduled post with this exact text existed before this run. False (with deleted also false) means there was nothing to cancel.
- `deleted` (boolean, required): True once the matching scheduled post was cancelled and confirmed gone from the panel.

## FAQ

### What does "LinkedIn — Cancel scheduled post" do?

Cancel one of the logged-in member's queued LinkedIn scheduled posts by its exact body text, via the Scheduled posts management panel. delete_post can't reach these — a scheduled post has no permalink until it actually publishes.

### How do I automatically cancel scheduled post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/remove_scheduled_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/remove_scheduled_post

### Is there a linkedin.com API to cancel scheduled post?

You do not need one. "LinkedIn — Cancel scheduled post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: text.

### What does it return?

It returns text, found, deleted.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/remove_scheduled_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/remove_scheduled_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/remove_scheduled_post
