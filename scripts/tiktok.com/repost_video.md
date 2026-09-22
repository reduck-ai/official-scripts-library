# Repost a TikTok video

Automatically repost a TikTok video on tiktok.com. Repost a TikTok video to your own profile, as the signed-in account, given the video's URL or id. A repost is public: it appears on the Reposts tab of your profile and can be shown to your followers, so confirm the exact video with the person asking before running this. The run first checks whether you have already reposted it and does nothing if so, echoes back whose video it is, and confirms afterwards that the repost really is on your profile. Use the list-user-reposts script to see reposts, including the ones this creates.

- Site: tiktok.com
- Address: `reduck/tiktok.com/repost_video`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/repost_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/repost_video
```

## Input

- `video` (string, required): Full TikTok video URL or a bare numeric video id.

## Output

- `videoId` (string, required)
- `reposted` (boolean, required): True when the video is reposted at the end of the run.
- `already_reposted` (boolean, required): True when it was already reposted before this run, so nothing was sent.
- `verified_on_profile` (boolean, required): True when a fresh read of your own reposts list shows the video.
- `author` (string | null, optional): Handle of the account whose video was reposted, echoed from the video page.
- `description` (string | null, optional): The video's caption, echoed from the video page so the caller can check the right video was reposted.
- `account_used` (string | null, optional): Handle the repost was published from, read from the signed-in session rather than assumed.
- `repostsScanned` (integer, optional): How many existing reposts were read to establish whether this one was already there.

## FAQ

### What does "Repost a TikTok video" do?

Repost a TikTok video to your own profile, as the signed-in account, given the video's URL or id. A repost is public: it appears on the Reposts tab of your profile and can be shown to your followers, so confirm the exact video with the person asking before running this. The run first checks whether you have already reposted it and does nothing if so, echoes back whose video it is, and confirms afterwards that the repost really is on your profile. Use the list-user-reposts script to see reposts, including the ones this creates.

### How do I automatically repost a TikTok video on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/repost_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/repost_video

### Is there a tiktok.com API to repost a TikTok video?

You do not need one. "Repost a TikTok video" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video.

### What does it return?

It returns author, videoId, reposted, description, account_used, repostsScanned, already_reposted, verified_on_profile.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/repost_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/repost_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/repost_video
