# LinkedIn — Delete post

Automatically delete post on linkedin.com. Permanently delete one of the logged-in member's own LinkedIn posts by its permalink, via the post's own control menu (••• > Delete post > confirm). If the post is already gone, it returns already_deleted instead of throwing an error. Refuses to guess on a post that isn't the account's own (no Delete option in the control menu).

- Site: linkedin.com
- Address: `reduck/linkedin.com/delete_post`
- Updated: 2026-08-20 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/delete_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/delete_post
```

## Input

- `url` (string, required): The post's permalink, e.g. https://www.linkedin.com/feed/update/urn:li:activity:.../ or urn:li:share:.../ — as returned by create_post, get_post, or get_profile_posts (repost permalinks work too). Query string is stripped.

## Output

- `url` (string, required): The permalink acted on (query string stripped).
- `deleted` (boolean, required): True once this run's own Delete confirmation went through.
- `account_used` (object, required): The real account the deletion was performed under, echoed from the session/UI.
- `already_deleted` (boolean, required): True only when the post was positively shown to be gone before this run acted — a rendered not-found state, or the activity absent from the account's own recent-activity feed. Never inferred from a missing control menu.
- `verified_on_page` (boolean, required): True if the script independently confirmed the deletion took effect — not just that the confirm click went through.

## FAQ

### What does "LinkedIn — Delete post" do?

Permanently delete one of the logged-in member's own LinkedIn posts by its permalink, via the post's own control menu (••• > Delete post > confirm). If the post is already gone, it returns already_deleted instead of throwing an error. Refuses to guess on a post that isn't the account's own (no Delete option in the control menu).

### How do I automatically delete post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/delete_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/delete_post

### Is there a linkedin.com API to delete post?

You do not need one. "LinkedIn — Delete post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, deleted, account_used, already_deleted, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/delete_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/delete_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/delete_post
