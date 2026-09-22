# Get YouTube video

Automatically get YouTube video on youtube.com. Get a single YouTube video's metadata from a watch URL or video id. Returns videoId, title, author, channelId, channelUrl, viewCount, likeCount, lengthSeconds, isLive, isPrivate, isUnlisted, isFamilySafe, category, keywords, thumbnails, uploadDate, publishDate, description, canonicalUrl. likeCount is null when the uploader hides likes, and canonicalUrl may point to a sibling video that YouTube picked as the indexable winner.

- Site: youtube.com
- Address: `reduck/youtube.com/get_video`
- Updated: 2026-08-14 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/get_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_video
```

## Input

- `video` (string, required): A YouTube video URL (watch?v=, youtu.be/, /shorts/, /embed/) or a bare 11-char video id.

## Output

- `title` (string, required)
- `videoId` (string, required)
- `author` (string | null, optional)
- `isLive` (boolean, optional)
- `category` (string | null, optional)
- `keywords` (array, optional)
- `channelId` (string | null, optional)
- `isPrivate` (boolean, optional)
- `likeCount` (number | null, optional): null when the uploader hides likes.
- `viewCount` (number | null, optional)
- `channelUrl` (string | null, optional)
- `isUnlisted` (boolean, optional)
- `thumbnails` (array, optional)
- `uploadDate` (string | null, optional)
- `description` (string | null, optional)
- `publishDate` (string | null, optional)
- `canonicalUrl` (string | null, optional): SEO canonical watch URL; may point to a sibling video the site elected as indexable winner.
- `isFamilySafe` (boolean, optional)
- `lengthSeconds` (number | null, optional)

## FAQ

### What does "Get YouTube video" do?

Get a single YouTube video's metadata from a watch URL or video id. Returns videoId, title, author, channelId, channelUrl, viewCount, likeCount, lengthSeconds, isLive, isPrivate, isUnlisted, isFamilySafe, category, keywords, thumbnails, uploadDate, publishDate, description, canonicalUrl. likeCount is null when the uploader hides likes, and canonicalUrl may point to a sibling video that YouTube picked as the indexable winner.

### How do I automatically get YouTube video on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_video

### Is there a youtube.com API to get YouTube video?

You do not need one. "Get YouTube video" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Required: video.

### What does it return?

It returns title, author, isLive, videoId, category, keywords, channelId, isPrivate, likeCount, viewCount, channelUrl, isUnlisted, thumbnails, uploadDate, description, publishDate, canonicalUrl, isFamilySafe, lengthSeconds.

### Do I need to be logged in to youtube.com?

No. It only uses pages of youtube.com that are reachable without signing in.

### Does it change anything on youtube.com, or only read data?

Unknown: its author has not declared whether it changes anything on youtube.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/get_video
