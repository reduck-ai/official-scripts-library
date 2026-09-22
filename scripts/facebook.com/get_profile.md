# Get Facebook profile info

Automatically get Facebook profile info on facebook.com. Get header and intro info for a Facebook profile or page (pass a URL or a bare id/username). Returns the type (profile or page), the name, friends, likes and follower counts as displayed, mutual friends, and the intro lines — bio plus city, work and education for people, or the description for pages. Counts come back as the strings Facebook shows (e.g. "11 K") and intro lines are returned as they appear, not sorted into city, work or school fields. Works in either the French or the English interface. An id or username Facebook will not serve returns a clear error rather than an empty record.

- Site: facebook.com
- Address: `reduck/facebook.com/get_profile`
- Updated: 2026-09-16 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/get_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_profile
```

## Input

- `profile` (string, required): Profile/page URL or bare id/username.

## Output

- `name` (string | null, required): Display name as shown on the header.
- `type` (string, required): What Facebook itself labels the target: a person/public-figure profile, or a Page.
- `intro` (array, required): Intro card lines as shown (bio, category, city, work, education, contact links), in page order and not classified into fields.
- `profileUrl` (string, required): Canonical profile/page URL, query string stripped.
- `likes` (string | null, optional): Like count exactly as displayed; null when the header shows no likes.
- `followers` (string | null, optional): Follower count exactly as displayed; null when the header shows no followers.
- `friendsCount` (string | null, optional): Friend count exactly as displayed (e.g. "1,2 K"); null on Pages and wherever Facebook does not show one.
- `mutualFriends` (string | null, optional): Mutual-friends line as displayed; null when there is none.

## FAQ

### What does "Get Facebook profile info" do?

Get header and intro info for a Facebook profile or page (pass a URL or a bare id/username). Returns the type (profile or page), the name, friends, likes and follower counts as displayed, mutual friends, and the intro lines — bio plus city, work and education for people, or the description for pages. Counts come back as the strings Facebook shows (e.g. "11 K") and intro lines are returned as they appear, not sorted into city, work or school fields. Works in either the French or the English interface. An id or username Facebook will not serve returns a clear error rather than an empty record.

### How do I automatically get Facebook profile info on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_profile

### Is there a facebook.com API to get Facebook profile info?

You do not need one. "Get Facebook profile info" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: profile.

### What does it return?

It returns name, type, intro, likes, followers, profileUrl, friendsCount, mutualFriends.

### Do I need to be logged in to facebook.com?

No. It only uses pages of facebook.com that are reachable without signing in.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/get_profile
