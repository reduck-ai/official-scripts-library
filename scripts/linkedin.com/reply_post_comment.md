# Reply to LinkedIn comment

Automatically reply to LinkedIn comment on linkedin.com. Reply to a specific comment on a LinkedIn post, by the post URL plus the comment's urn (from get_post_comments or comment_post). Posts a real public reply under the logged-in account. The whole comment thread is paged through to reach the target, so a comment far down a long list is still found; replies that LinkedIn keeps hidden behind a "see previous replies" link are not expanded. The reply box auto-@mentions the comment author, and your text is added after that mention. Returns replied, plus the new reply's urn.

- Site: linkedin.com
- Address: `reduck/linkedin.com/reply_post_comment`
- Updated: 2026-08-24 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/reply_post_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/reply_post_comment
```

## Input

- `reply` (string, required): The reply text. This posts a real, public reply under the user's account immediately, so confirm the exact text with them before running.
- `postUrl` (string, required): LinkedIn post permalink (/feed/update/urn:li:activity:.../).
- `commentUrn` (string, required): The target comment's urn, e.g. urn:li:comment:(activity:123,456) (from get_post_comments / comment_post).

## Output

- `reply` (string, required)
- `postUrl` (string, required)
- `replied` (boolean, required)
- `commentUrn` (string, required): The TARGET comment's urn (the one replied to).
- `account_used` (object, required): The real account the reply was (or would be) posted under, echoed from the session/UI.
- `already_present` (boolean, required): True if an exact-text reply was found already loaded under this comment's activity before opening the reply composer. Best-effort: a false does not guarantee no duplicate exists behind an unexpanded 'see previous replies' link.
- `verified_on_page` (boolean, required): True if the script independently re-inspected the newly created reply node's own rendered text and confirmed it matches what was posted. Always true when already_present is true.
- `replyUrn` (string | null, optional): urn:li:comment of the CREATED reply, from the create response; null if unresolved. Points at the pre-existing reply instead when already_present is true.

## FAQ

### What does "Reply to LinkedIn comment" do?

Reply to a specific comment on a LinkedIn post, by the post URL plus the comment's urn (from get_post_comments or comment_post). Posts a real public reply under the logged-in account. The whole comment thread is paged through to reach the target, so a comment far down a long list is still found; replies that LinkedIn keeps hidden behind a "see previous replies" link are not expanded. The reply box auto-@mentions the comment author, and your text is added after that mention. Returns replied, plus the new reply's urn.

### How do I automatically reply to LinkedIn comment on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/reply_post_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/reply_post_comment

### Is there a linkedin.com API to reply to LinkedIn comment?

You do not need one. "Reply to LinkedIn comment" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl, commentUrn, reply.

### What does it return?

It returns reply, postUrl, replied, replyUrn, commentUrn, account_used, already_present, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/reply_post_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/reply_post_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/reply_post_comment
