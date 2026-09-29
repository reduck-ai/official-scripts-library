# Post photos to TikTok

Automatically post photos to TikTok on tiktok.com. Publish a photo post with a caption on the signed-in TikTok account, through TikTok Studio. Runs in practice mode by default: it uploads the image and fills the caption, then stops before Post. Pass dryRun:false to publish for real; it then re-reads your profile and returns the new post's id and URL. Posting is public and immediate, so show the exact image and caption to the person and get their confirmation first. Use the delete-post script to remove it.

- Site: tiktok.com
- Address: `reduck/tiktok.com/create_photo_post`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/create_photo_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/create_photo_post
```

## Input

- `photo` (string, required): Image to post (JPEG, PNG or WebP).
- `caption` (string, required): Post description, up to 4000 characters.
- `dryRun` (boolean, optional): Practice mode (default true): uploads and fills the caption, then stops before Post. Pass false to publish for real.

## FAQ

### What does "Post photos to TikTok" do?

Publish a photo post with a caption on the signed-in TikTok account, through TikTok Studio. Runs in practice mode by default: it uploads the image and fills the caption, then stops before Post. Pass dryRun:false to publish for real; it then re-reads your profile and returns the new post's id and URL. Posting is public and immediate, so show the exact image and caption to the person and get their confirmation first. Use the delete-post script to remove it.

### How do I automatically post photos to TikTok on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/create_photo_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/create_photo_post

### Is there a tiktok.com API to post photos to TikTok?

You do not need one. "Post photos to TikTok" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: photo, caption. Optional: dryRun.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/create_photo_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/create_photo_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/create_photo_post
