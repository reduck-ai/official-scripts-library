# Delete a TikTok post

Automatically delete a TikTok post on tiktok.com. Delete one of your own TikTok posts (video or photo), given its URL or id, from the TikTok Studio posts list. Runs in practice mode by default: it finds the post and opens its Delete option, then stops. Pass dryRun:false to delete for real; it confirms the dialog, then reloads the list to prove the post is gone. If the post isn't in your list, it reports alreadyAbsent instead of failing, so repeating it is safe. TikTok keeps deleted posts in Recently deleted for 30 days.

- Site: tiktok.com
- Address: `reduck/tiktok.com/delete_video`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/delete_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/delete_video
```

## Input

- `video` (string, required): URL or numeric id of one of your own TikTok posts (video or photo).
- `dryRun` (boolean, optional): Practice mode (default true): finds the post and opens its Delete option, then stops. Pass false to delete for real (cannot be undone).

## Output

- `id` (string, optional)
- `dryRun` (boolean, optional)
- `deleted` (boolean, optional)
- `alreadyAbsent` (boolean, optional)

## FAQ

### What does "Delete a TikTok post" do?

Delete one of your own TikTok posts (video or photo), given its URL or id, from the TikTok Studio posts list. Runs in practice mode by default: it finds the post and opens its Delete option, then stops. Pass dryRun:false to delete for real; it confirms the dialog, then reloads the list to prove the post is gone. If the post isn't in your list, it reports alreadyAbsent instead of failing, so repeating it is safe. TikTok keeps deleted posts in Recently deleted for 30 days.

### How do I automatically delete a TikTok post on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/delete_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/delete_video

### Is there a tiktok.com API to delete a TikTok post?

You do not need one. "Delete a TikTok post" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video. Optional: dryRun.

### What does it return?

It returns id, dryRun, deleted, alreadyAbsent.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/delete_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/delete_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/delete_video
