# Get TikTok music info

Automatically get TikTok music info on tiktok.com. Get a TikTok sound's metadata by music id: title, author, duration, video count, original/commercial flags, cover and play URL. Complements get_music_videos (which lists the videos using the sound).

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_music_info`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_music_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_music_info
```

## Input

- `musicId` (string, required): Numeric TikTok music/sound id (e.g. from get_video's music, or a /music/...-<id> URL).

## Output

- `id` (string, required)
- `title` (string, required)
- `videoCount` (number, required): Number of videos using this sound.
- `cover` (string | null, optional): Cover image URL. Signed, expires within hours.
- `author` (object | null, optional): The TikTok account that owns the sound (for original sounds, the creator).
- `playUrl` (string | null, optional): Audio stream URL. Signed, expires within hours.
- `duration` (number | null, optional): Usable clip length in seconds.
- `original` (boolean, optional): True for an original creator sound (not a licensed track).
- `authorName` (string | null, optional): Credited sound author name.
- `isCommerce` (boolean, optional): Commercial/licensed music library track.
- `isCopyrighted` (boolean, optional)

## FAQ

### What does "Get TikTok music info" do?

Get a TikTok sound's metadata by music id: title, author, duration, video count, original/commercial flags, cover and play URL. Complements get_music_videos (which lists the videos using the sound).

### How do I automatically get TikTok music info on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_music_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_music_info

### Is there a tiktok.com API to get TikTok music info?

You do not need one. "Get TikTok music info" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: musicId.

### What does it return?

It returns id, cover, title, author, playUrl, duration, original, authorName, isCommerce, videoCount, isCopyrighted.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_music_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_music_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_music_info
