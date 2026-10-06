# Get Instagram story viewers

Automatically get Instagram story viewers on instagram.com. List who has viewed your currently active Instagram stories. For each live story item, returns its id, posted and expiry times, photo or video, the total viewer count Instagram reports, and the viewers (id, username, full name, verified badge, profile picture). Pass storyId to read a single item, and limit to cap viewers per item (default 100); truncated tells you when there are more. hasActiveStory is false when nothing is live, since stories expire after 24h. Read-only. It only covers the signed-in account's own stories.

- Site: instagram.com
- Address: `reduck/instagram.com/get_story_viewers`
- Updated: 2026-10-05 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_story_viewers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_story_viewers
```

## Input

- `limit` (integer, optional): Maximum viewers to return per story item.
- `storyId` (string, optional): Optional: id of one of your active story items. Omit to return viewers for every active story item.

## Output

- `stories` (array, required)
- `username` (string, required)
- `hasActiveStory` (boolean, required): False when you have no story live right now (stories expire after 24h); stories is then empty.
- `userId` (string, optional)

## FAQ

### What does "Get Instagram story viewers" do?

List who has viewed your currently active Instagram stories. For each live story item, returns its id, posted and expiry times, photo or video, the total viewer count Instagram reports, and the viewers (id, username, full name, verified badge, profile picture). Pass storyId to read a single item, and limit to cap viewers per item (default 100); truncated tells you when there are more. hasActiveStory is false when nothing is live, since stories expire after 24h. Read-only. It only covers the signed-in account's own stories.

### How do I automatically get Instagram story viewers on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_story_viewers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_story_viewers

### Is there a instagram.com API to get Instagram story viewers?

You do not need one. "Get Instagram story viewers" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Optional: limit, storyId.

### What does it return?

It returns userId, stories, username, hasActiveStory.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_story_viewers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_story_viewers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_story_viewers
