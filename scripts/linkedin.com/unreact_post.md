# Remove reaction from LinkedIn post

Automatically remove reaction from LinkedIn post on linkedin.com. Remove your reaction (undo the Like/Celebrate/etc.) from a LinkedIn post by its permalink. Applies to the main post, not per-comment reactions. Idempotent (returns not_reacted if you hadn't reacted); statuses unreacted/not_reacted.

- Site: linkedin.com
- Address: `reduck/linkedin.com/unreact_post`
- Updated: 2026-09-03 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/unreact_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unreact_post
```

## Input

- `postUrl` (string, required): LinkedIn post permalink, e.g. https://www.linkedin.com/feed/update/urn:li:activity:123.../ or https://www.linkedin.com/posts/<slug>.

## Output

- `status` (string, required)
- `postUrl` (string, required)
- `account_used` (object, required): The real account the removal was performed under, echoed from the session/UI.
- `verified_on_page` (boolean, required): True if the script independently reloaded the post permalink and confirmed the reaction button's aria-pressed state is now false, not just that the click's own in-page state change fired. Always true on a not_reacted hit (the pre-existing state was what was matched).

## FAQ

### What does "Remove reaction from LinkedIn post" do?

Remove your reaction (undo the Like/Celebrate/etc.) from a LinkedIn post by its permalink. Applies to the main post, not per-comment reactions. Idempotent (returns not_reacted if you hadn't reacted); statuses unreacted/not_reacted.

### How do I automatically remove reaction from LinkedIn post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/unreact_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unreact_post

### Is there a linkedin.com API to remove reaction from LinkedIn post?

You do not need one. "Remove reaction from LinkedIn post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl.

### What does it return?

It returns status, postUrl, account_used, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/unreact_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unreact_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/unreact_post
