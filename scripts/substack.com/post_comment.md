# Post Substack comment

Automatically post Substack comment on substack.com. Post a comment on a Substack post as the logged-in account. The account needs a display name set up on Substack first (via any post's comment box) — the script fails loudly with instructions if it isn't.

- Site: substack.com
- Address: `reduck/substack.com/post_comment`
- Updated: 2026-08-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/substack.com/post_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/substack.com/post_comment
```

## Input

- `url` (string, required): Full URL of the Substack post, e.g. https://example.substack.com/p/my-post-slug
- `text` (string, required): The comment text to post

## Output

- `url` (string, required)
- `text` (string, required)
- `postId` (number, required)
- `postedAt` (string, required)
- `commentId` (number, required)

## FAQ

### What does "Post Substack comment" do?

Post a comment on a Substack post as the logged-in account. The account needs a display name set up on Substack first (via any post's comment box) — the script fails loudly with instructions if it isn't.

### How do I automatically post Substack comment on substack.com?

Ask an AI agent connected to Reduck to run reduck/substack.com/post_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/post_comment

### Is there a substack.com API to post Substack comment?

You do not need one. "Post Substack comment" drives the real substack.com pages in a browser, so it works whether or not substack.com offers an API for this.

### What information do I need to provide?

Required: url, text.

### What does it return?

It returns url, text, postId, postedAt, commentId.

### Do I need to be logged in to substack.com?

Yes. It acts as you on substack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the substack.com cookies saved by the Reduck extension.

### Does it change anything on substack.com, or only read data?

It makes changes on substack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/substack.com/post_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/post_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/substack.com/post_comment
