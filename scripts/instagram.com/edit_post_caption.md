# Edit an Instagram post's caption

Automatically edit an Instagram post's caption on instagram.com. Edit the caption of one of the signed-in account's own Instagram posts, given the post's code (from its /p/&lt;code&gt;/ URL or list_scripts' post-listing methods). Opens the post's own Edit info dialog, replaces the caption text, and saves. Only works on posts you own.

- Site: instagram.com
- Address: `reduck/instagram.com/edit_post_caption`
- Updated: 2026-09-21 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/edit_post_caption`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/edit_post_caption
```

## Input

- `code` (string, required): The post's code, the /p/<code>/ URL segment
- `caption` (string, required): New caption text to replace the current one

## Output

- `code` (string, required)
- `edited` (boolean, required)
- `caption` (string, required)

## FAQ

### What does "Edit an Instagram post's caption" do?

Edit the caption of one of the signed-in account's own Instagram posts, given the post's code (from its /p/&lt;code&gt;/ URL or list_scripts' post-listing methods). Opens the post's own Edit info dialog, replaces the caption text, and saves. Only works on posts you own.

### How do I automatically edit an Instagram post's caption on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/edit_post_caption, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/edit_post_caption

### Is there a instagram.com API to edit an Instagram post's caption?

You do not need one. "Edit an Instagram post's caption" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: code, caption.

### What does it return?

It returns code, edited, caption.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/edit_post_caption, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/edit_post_caption

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/edit_post_caption
