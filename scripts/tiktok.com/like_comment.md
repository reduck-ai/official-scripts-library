# Like TikTok Comment

Automatically like TikTok Comment on tiktok.com. Pass the text of one top-level comment and find out whether its heart was already on or is on now.

- Site: tiktok.com
- Address: `reduck/tiktok.com/like_comment`
- Updated: 2026-10-05 (v4)
- Author: Reduck AI (reduck)

## About

On your own videos, your heart puts a "Liked by creator" label under the viewer's comment, a public sign you read it. A bakery that posts a croissant video at 8am can have an agent sort the comments at lunch: pull them with get_comments, skip the ones already marked likedByCreator, heart the twelve friendly ones with this script (one run per comment) and answer the two questions about opening hours with reply_to_comment. Each run opens the comment panel in your signed-in Chrome and hearts the single top-level row that matches. If liked comes back false, the heart did not stay on after the click, so check the video before trying again. The weak spot is matching. With no comment id in the panel, the script looks for a comment containing your text, ignoring case, so a bare "so good" also hits "omg so good". Paste the whole comment. Only the comments the panel loads first are searched, too.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/like_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/like_comment
```

## Input

- `videoUrl` (string, required): The video's canonical URL, e.g. https://www.tiktok.com/@someuser/video/1234567890123456789.
- `commentText` (string, required): The exact, full text of the top-level comment to like, as it appears on the video. Comments have no visible ID in the UI, so text is the only handle a caller can read off the page — it must match exactly (including emoji), and must be unique among top-level comments on the video.

## Output

- `liked` (boolean, required)
- `video_url` (string, required)
- `comment_text` (string, required)
- `already_liked` (boolean, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "liked": true,
  "video_url": "https://example.com/item/123",
  "comment_text": "…",
  "already_liked": true
}
```

## FAQ

### What does "Like TikTok Comment" do?

Likes a top-level comment on a public TikTok video, matched by its exact text. Idempotent — already-liked comments are reported, not re-liked.

### How do I automatically like TikTok Comment on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/like_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/like_comment

### Is there a tiktok.com API to like TikTok Comment?

You do not need one. "Like TikTok Comment" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: videoUrl, commentText.

### What does it return?

It returns liked, video_url, comment_text, already_liked.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/like_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/like_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Why does it say 3 comments matched when only one person wrote "fire"?

Matching looks for top-level comments that contain your text, ignoring case, so "fire" also hits "this is fire" and "FIRE omg". Pass a longer, distinctive stretch of the comment, ideally the whole text as get_comments returns it. A comment that is only a sticker has no text to match, so this script cannot target it.

### Why does it say no comment matched when I can see the comment on TikTok?

The script reads only the comments the panel loads when it first opens and never scrolls, so a comment far down a busy video can be out of reach. Capitalisation does not matter and a leading or trailing emoji can be left off, but a typo inside the text gives no match. The same limit cuts the other way: if the comment you meant is out of reach and only one loaded comment contains your text, that one gets the heart instead.

### Why does it want the comment text instead of the id get_comments gives me?

Liking happens in the comment panel on the video page, and that panel shows no comment id, so the script finds the row by its text. Keep the id from get_comments for reply_to_comment or delete_comment, which take it directly.

### Can it like a reply under a comment?

Only top-level comments, the ones listed directly under the video, can be liked with this script, because it never opens reply threads. The get_comment_replies script can read replies, but Reduck has no script that likes them.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/like_comment
