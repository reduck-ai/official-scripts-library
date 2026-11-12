# Get an Instagram post

Automatically get an Instagram post on instagram.com. Read one Instagram post or reel by its shortcode, the X in instagram.com/p/X/ or instagram.com/reel/X/. Returns its id, type (photo, video or carousel), when it was posted, the caption, the author, coauthors, like, comment and repost counts, location, tagged accounts, paid-partnership flags, size, the image and video links, and each item of a carousel. like_count is null when the author hides likes, which like_count_hidden says. Image and video links are signed and expire after some days, so download what you need to keep. A post that was removed, is private to this account, or a wrong code fails with a message that says so. For the comments use instagram.com/get_post_comments, and for who liked it instagram.com/get_post_likers.

- Site: instagram.com
- Address: `reduck/instagram.com/get_post`
- Updated: 2026-11-11 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post
```

## Input

- `code` (string, required): The post's shortcode, the X in instagram.com/p/X/ or instagram.com/reel/X/, or that whole link. instagram.com/get_user_posts returns it as code.

## Output

- `url` (string, required)
- `code` (string, required)
- `id` (string | null, optional): Instagram's numeric media id.
- `width` (integer | null, optional)
- `author` (object | null, optional)
- `height` (integer | null, optional)
- `caption` (string | null, optional)
- `carousel` (array, optional): Each item of a carousel, in order; empty for a single photo or video.
- `location` (object | null, optional)
- `taken_at` (string | null, optional): When it was posted, ISO datetime.
- `coauthors` (array, optional): Usernames of the other accounts the post is published with.
- `image_url` (string | null, optional): The post's image, or the cover of a video or the first item of a carousel.
- `video_url` (string | null, optional)
- `like_count` (integer | null, optional): Null when the author hides likes.
- `media_type` (any, optional)
- `view_count` (integer | null, optional): Null when Instagram does not show it on the post's page, as for most reels.
- `product_type` (string | null, optional): Instagram's own kind of post: feed, clips (a reel), carousel_container, igtv.
- `repost_count` (integer | null, optional)
- `sponsor_tags` (array, optional)
- `tagged_users` (array, optional)
- `comment_count` (integer | null, optional)
- `video_duration` (number | null, optional): Seconds.
- `caption_is_edited` (boolean, optional)
- `comments_disabled` (boolean, optional)
- `like_count_hidden` (boolean, optional)
- `is_paid_partnership` (boolean, optional)

## FAQ

### What does "Get an Instagram post" do?

Read one Instagram post or reel by its shortcode, the X in instagram.com/p/X/ or instagram.com/reel/X/. Returns its id, type (photo, video or carousel), when it was posted, the caption, the author, coauthors, like, comment and repost counts, location, tagged accounts, paid-partnership flags, size, the image and video links, and each item of a carousel. like_count is null when the author hides likes, which like_count_hidden says. Image and video links are signed and expire after some days, so download what you need to keep. A post that was removed, is private to this account, or a wrong code fails with a message that says so. For the comments use instagram.com/get_post_comments, and for who liked it instagram.com/get_post_likers.

### How do I automatically get an Instagram post on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post

### Is there a instagram.com API to get an Instagram post?

You do not need one. "Get an Instagram post" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: code.

### What does it return?

It returns id, url, code, width, author, height, caption, carousel, location, taken_at, coauthors, image_url, video_url, like_count, media_type, view_count, product_type, repost_count, sponsor_tags, tagged_users, comment_count, video_duration, caption_is_edited, comments_disabled, like_count_hidden, is_paid_partnership.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_post
