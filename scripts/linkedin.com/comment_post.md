# Comment on LinkedIn post

Automatically comment on LinkedIn post on linkedin.com. Post a top-level comment on a LinkedIn post by its permalink. Posts a real public comment under the logged-in account. Only comments on the main post, not a reply thread. Returns the new comment's permalink so you can reply to it afterward.

- Site: linkedin.com
- Address: `reduck/linkedin.com/comment_post`
- Updated: 2026-08-24 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/comment_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/comment_post
```

## Input

- `comment` (string, required): The comment text to post. This posts a real, public comment under the user's account immediately, so confirm the exact text with them before running.
- `postUrl` (string, required): LinkedIn post permalink (/feed/update/urn:li:activity:.../ or /posts/...).
- `mentions` (array, optional): Person or organization names to mention, appended in order at the end of comment and resolved through the comment box's own mention typeahead. Confirm each name with the user before running. If a name is ambiguous (several people share it exactly), the run throws and lists the candidates by headline — re-run with the name plus enough of their headline, company or organization for LinkedIn's typeahead to narrow to exactly one match; this works even though the matched suggestion still displays just the plain name.

## Output

- `posted` (boolean, required)
- `comment` (string, required)
- `postUrl` (string, required)
- `account_used` (object, required)
- `already_present` (boolean, required)
- `verified_on_page` (boolean, required)
- `commentUrn` (string | null, optional)

## FAQ

### What does "Comment on LinkedIn post" do?

Post a top-level comment on a LinkedIn post by its permalink. Posts a real public comment under the logged-in account. Only comments on the main post, not a reply thread. Returns the new comment's permalink so you can reply to it afterward.

### How do I automatically comment on LinkedIn post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/comment_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/comment_post

### Is there a linkedin.com API to comment on LinkedIn post?

You do not need one. "Comment on LinkedIn post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl, comment. Optional: mentions.

### What does it return?

It returns posted, comment, postUrl, commentUrn, account_used, already_present, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/comment_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/comment_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/comment_post
