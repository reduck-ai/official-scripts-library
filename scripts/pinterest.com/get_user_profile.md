# Get Pinterest user profile

Automatically get Pinterest user profile on pinterest.com. Fetches a Pinterest user/brand profile's public details by username: display name, bio, avatar, follower count, external links, join date. Read-only, no login required. Board count/pin count/following count are not exposed on this page for anonymous viewers, so they are omitted rather than guessed.

- Site: pinterest.com
- Address: `reduck/pinterest.com/get_user_profile`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pinterest.com/get_user_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pinterest.com/get_user_profile
```

## Input

- `username` (string, required): Pinterest username/handle, e.g. "natgeo"

## Output

- `url` (string, required)
- `username` (string, required)
- `bio` (string | null, optional)
- `links` (array, optional)
- `fullName` (string | null, optional)
- `imageUrl` (string | null, optional)
- `createdAt` (string | null, optional)
- `followerCount` (integer | null, optional)

## FAQ

### What does "Get Pinterest user profile" do?

Fetches a Pinterest user/brand profile's public details by username: display name, bio, avatar, follower count, external links, join date. Read-only, no login required. Board count/pin count/following count are not exposed on this page for anonymous viewers, so they are omitted rather than guessed.

### How do I automatically get Pinterest user profile on pinterest.com?

Ask an AI agent connected to Reduck to run reduck/pinterest.com/get_user_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pinterest.com/get_user_profile

### Is there a pinterest.com API to get Pinterest user profile?

You do not need one. "Get Pinterest user profile" drives the real pinterest.com pages in a browser, so it works whether or not pinterest.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns bio, url, links, fullName, imageUrl, username, createdAt, followerCount.

### Do I need to be logged in to pinterest.com?

No. It only uses pages of pinterest.com that are reachable without signing in.

### Does it change anything on pinterest.com, or only read data?

It only reads. It looks things up on pinterest.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pinterest.com/get_user_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pinterest.com/get_user_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pinterest.com/get_user_profile
