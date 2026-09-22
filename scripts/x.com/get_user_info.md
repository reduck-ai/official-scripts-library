# Get X user info

Automatically get X user info on x.com. Look up an X user's profile by handle. Returns handle, user_id, name, bio, location, website, joined, followers_count, following_count, is_verified, is_self, is_following, follows_you. Follower/following counts are exact integers, not X's abbreviated "3.7M" display text. bio and website carry the real destination URLs, with X's t.co shortlinks resolved. is_following is null on your own profile (you have no follow relationship to yourself); user_id is always present.

- Site: x.com
- Address: `reduck/x.com/get_user_info`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_user_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_info
```

## Input

- `handle` (string, required): X handle without the leading @. Case-insensitive; the result carries the canonical casing.

## Output

- `name` (string, required)
- `handle` (string, required): Canonical handle as returned by X (may differ in casing from the input).
- `is_self` (boolean, required): True when this profile is the signed-in viewer's own.
- `user_id` (string, required): Numeric rest_id. Always present, including your own profile.
- `follows_you` (boolean, required): Whether they follow you.
- `is_verified` (boolean, required): Blue/verified badge (is_blue_verified).
- `is_following` (boolean | null, required): Whether you follow them; null on your own profile.
- `bio` (string | null, optional): Profile bio text, with any t.co shortlinks replaced by their real destination (as the page displays them); null when empty.
- `joined` (string | null, optional): Account creation date in X's format, e.g. 'Tue Jun 02 20:12:29 +0000 2009'.
- `website` (string | null, optional): Expanded profile URL (the full destination link, not the t.co shortlink or the display text); null when the profile has none.
- `location` (string | null, optional): Profile location; null when empty.
- `followers_count` (integer | null, optional): Exact follower count as an integer (not X's abbreviated '1.3M' display string).
- `following_count` (integer | null, optional): Exact count of accounts this profile follows; 0 is a real value.

## FAQ

### What does "Get X user info" do?

Look up an X user's profile by handle. Returns handle, user_id, name, bio, location, website, joined, followers_count, following_count, is_verified, is_self, is_following, follows_you. Follower/following counts are exact integers, not X's abbreviated "3.7M" display text. bio and website carry the real destination URLs, with X's t.co shortlinks resolved. is_following is null on your own profile (you have no follow relationship to yourself); user_id is always present.

### How do I automatically get X user info on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_info

### Is there a x.com API to get X user info?

You do not need one. "Get X user info" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle.

### What does it return?

It returns bio, name, handle, joined, is_self, user_id, website, location, follows_you, is_verified, is_following, followers_count, following_count.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

Unknown: its author has not declared whether it changes anything on x.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_user_info
