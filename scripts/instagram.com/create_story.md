# Post an Instagram story

Automatically post an Instagram story on instagram.com. Publish a photo to the signed-in Instagram account's story. Pass the image as the attachment file input, a direct image_url, or small image_base64 (JPEG, PNG, WebP or GIF; converted to JPEG). Instagram's desktop site has no story creation, so this drives its mobile site. It works whether or not a story is already live. Practice mode by default: it loads the photo into Instagram's story editor and stops before publishing. Pass dry_run:false to publish for real; it then confirms from Instagram's own response AND by re-reading your active stories, and returns the story id, link and expiry time. Stories are visible to your audience for 24 hours, so show the exact photo to the person and get their confirmation first. Pair with get_story_viewers to see who watched.

- Site: instagram.com
- Address: `reduck/instagram.com/create_story`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/create_story`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/create_story
```

## Input

- `dry_run` (boolean, optional): Practice mode (default true): loads the photo into Instagram's story editor and stops before publishing. Pass false to publish for real — stories are public to your audience for 24 hours.
- `image_url` (string, optional): Direct URL of the photo to post, fetched by the browser itself.
- `attachment` (string, optional): The photo to post (JPEG, PNG, WebP or GIF), passed through the platform's file channel. No size cap.
- `image_base64` (string, optional): The photo's bytes as base64 or a data: URL. Small images only (the request is capped near 100KB); prefer attachment or image_url.

## Output

- `posted` (boolean, required)
- `dry_run` (boolean, required)
- `username` (string, required): The account the story was (or would be) published from.
- `url` (string | null, optional)
- `width` (integer, optional)
- `height` (integer, optional)
- `storyId` (string | null, optional): Id of the new story item; usable with get_story_viewers.
- `expiresAt` (string | null, optional)

## FAQ

### What does "Post an Instagram story" do?

Publish a photo to the signed-in Instagram account's story. Pass the image as the attachment file input, a direct image_url, or small image_base64 (JPEG, PNG, WebP or GIF; converted to JPEG). Instagram's desktop site has no story creation, so this drives its mobile site. It works whether or not a story is already live. Practice mode by default: it loads the photo into Instagram's story editor and stops before publishing. Pass dry_run:false to publish for real; it then confirms from Instagram's own response AND by re-reading your active stories, and returns the story id, link and expiry time. Stories are visible to your audience for 24 hours, so show the exact photo to the person and get their confirmation first. Pair with get_story_viewers to see who watched.

### How do I automatically post an Instagram story on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/create_story, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/create_story

### Is there a instagram.com API to post an Instagram story?

You do not need one. "Post an Instagram story" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Optional: dry_run, image_url, attachment, image_base64.

### What does it return?

It returns url, width, height, posted, dry_run, storyId, username, expiresAt.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/create_story, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/create_story

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/create_story
