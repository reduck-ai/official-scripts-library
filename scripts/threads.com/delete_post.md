# Delete Threads post

Automatically delete Threads post on threads.com. Delete a post or reply owned by the logged-in Threads account.

- Site: threads.com
- Address: `reduck/threads.com/delete_post`
- Updated: 2026-08-27 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/threads.com/delete_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/threads.com/delete_post
```

## Input

- `postId` (string, required): The post or reply's id, from its URL /@username/post/<postId>
- `username` (string, required): Author's Threads username of the post/reply to delete (without @) — must be the logged-in account

## Output

- `postId` (string, required)
- `deleted` (boolean, required)

## FAQ

### What does "Delete Threads post" do?

Delete a post or reply owned by the logged-in Threads account.

### How do I automatically delete Threads post on threads.com?

Ask an AI agent connected to Reduck to run reduck/threads.com/delete_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/delete_post

### Is there a threads.com API to delete Threads post?

You do not need one. "Delete Threads post" drives the real threads.com pages in a browser, so it works whether or not threads.com offers an API for this.

### What information do I need to provide?

Required: username, postId.

### What does it return?

It returns postId, deleted.

### Do I need to be logged in to threads.com?

Yes. It acts as you on threads.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the threads.com cookies saved by the Reduck extension.

### Does it change anything on threads.com, or only read data?

It makes changes on threads.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/threads.com/delete_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/delete_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/threads.com/delete_post
