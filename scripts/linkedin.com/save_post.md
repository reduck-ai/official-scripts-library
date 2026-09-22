# Save LinkedIn post

Automatically save LinkedIn post on linkedin.com. Save a LinkedIn post to your saved items (My Items > Saved posts) by its permalink. Returns already_saved if the post was already saved, or saved otherwise.

- Site: linkedin.com
- Address: `reduck/linkedin.com/save_post`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/save_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/save_post
```

## Input

- `postUrl` (string, required): LinkedIn post permalink, e.g. https://www.linkedin.com/feed/update/urn:li:activity:123.../ or https://www.linkedin.com/posts/<slug>.

## Output

- `status` (string, required)
- `postUrl` (string, required)
- `verified_on_page` (boolean, required): True if reopening the post's control menu after the action independently confirmed the saved (Unsave) state - not just that the click's own in-page state change fired.

## FAQ

### What does "Save LinkedIn post" do?

Save a LinkedIn post to your saved items (My Items > Saved posts) by its permalink. Returns already_saved if the post was already saved, or saved otherwise.

### How do I automatically save LinkedIn post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/save_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/save_post

### Is there a linkedin.com API to save LinkedIn post?

You do not need one. "Save LinkedIn post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl.

### What does it return?

It returns status, postUrl, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/save_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/save_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/save_post
