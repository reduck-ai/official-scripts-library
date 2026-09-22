# Create Threads post

Automatically create Threads post on threads.com. Publish a new text post (thread) to Threads from the logged-in account.

- Site: threads.com
- Address: `reduck/threads.com/create_post`
- Updated: 2026-09-04 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/threads.com/create_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/threads.com/create_post
```

## Input

- `text` (string, required): Post body, max 500 characters (Threads' own limit).

## Output

- `text` (string, required)
- `username` (string, required)
- `published` (boolean, required)
- `postId` (string | null, optional)
- `createdAt` (string | null, optional)
- `permalink` (string | null, optional)

## FAQ

### What does "Create Threads post" do?

Publish a new text post (thread) to Threads from the logged-in account.

### How do I automatically create Threads post on threads.com?

Ask an AI agent connected to Reduck to run reduck/threads.com/create_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/create_post

### Is there a threads.com API to create Threads post?

You do not need one. "Create Threads post" drives the real threads.com pages in a browser, so it works whether or not threads.com offers an API for this.

### What information do I need to provide?

Required: text.

### What does it return?

It returns text, postId, username, createdAt, permalink, published.

### Do I need to be logged in to threads.com?

Yes. It acts as you on threads.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the threads.com cookies saved by the Reduck extension.

### Does it change anything on threads.com, or only read data?

It makes changes on threads.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/threads.com/create_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/create_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/threads.com/create_post
