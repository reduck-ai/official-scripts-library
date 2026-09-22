# Reply to Threads post

Automatically reply to Threads post on threads.com. Publish a text reply to a specific Threads post from the logged-in account.

- Site: threads.com
- Address: `reduck/threads.com/reply_to_post`
- Updated: 2026-08-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/threads.com/reply_to_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/threads.com/reply_to_post
```

## Input

- `text` (string, required): Text to publish as the reply
- `postId` (string, required): The post's id, from its URL /@username/post/<postId>
- `username` (string, required): Author's Threads username of the post being replied to (without @)

## Output

- `text` (string, required)
- `published` (boolean, required): true once the reply row's submit control was replaced by a spinner/confirmation
- `replyId` (string | null, optional): null if the new reply hadn't propagated into the thread within the wait window
- `createdAt` (string | null, optional)
- `permalink` (string | null, optional)

## FAQ

### What does "Reply to Threads post" do?

Publish a text reply to a specific Threads post from the logged-in account.

### How do I automatically reply to Threads post on threads.com?

Ask an AI agent connected to Reduck to run reduck/threads.com/reply_to_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/reply_to_post

### Is there a threads.com API to reply to Threads post?

You do not need one. "Reply to Threads post" drives the real threads.com pages in a browser, so it works whether or not threads.com offers an API for this.

### What information do I need to provide?

Required: username, postId, text.

### What does it return?

It returns text, replyId, createdAt, permalink, published.

### Do I need to be logged in to threads.com?

Yes. It acts as you on threads.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the threads.com cookies saved by the Reduck extension.

### Does it change anything on threads.com, or only read data?

It makes changes on threads.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/threads.com/reply_to_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/reply_to_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/threads.com/reply_to_post
