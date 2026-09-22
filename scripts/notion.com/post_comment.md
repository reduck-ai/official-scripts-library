# Post a comment on a Notion page

Automatically post a comment on a Notion page on notion.com. Posts a comment on a Notion page under the signed-in account, given the page's URL and the comment text. Returns the text that was posted and confirmation that it now appears on the page.

- Site: notion.com
- Address: `reduck/notion.com/post_comment`
- Updated: 2026-09-16 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notion.com/post_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notion.com/post_comment
```

## Input

- `text` (string, required): The comment text to post.
- `pageUrl` (string, required): URL of the Notion page to comment on.

## Output

- `text` (string, required)
- `posted` (boolean, required)
- `account` (string, required): The Notion account name the comment was posted as, read from the page after posting.

## FAQ

### What does "Post a comment on a Notion page" do?

Posts a comment on a Notion page under the signed-in account, given the page's URL and the comment text. Returns the text that was posted and confirmation that it now appears on the page.

### How do I automatically post a comment on a Notion page on notion.com?

Ask an AI agent connected to Reduck to run reduck/notion.com/post_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notion.com/post_comment

### Is there a notion.com API to post a comment on a Notion page?

You do not need one. "Post a comment on a Notion page" drives the real notion.com pages in a browser, so it works whether or not notion.com offers an API for this.

### What information do I need to provide?

Required: pageUrl, text.

### What does it return?

It returns text, posted, account.

### Do I need to be logged in to notion.com?

Yes. It acts as you on notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the notion.com cookies saved by the Reduck extension.

### Does it change anything on notion.com, or only read data?

It makes changes on notion.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notion.com/post_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notion.com/post_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/notion.com/post_comment
