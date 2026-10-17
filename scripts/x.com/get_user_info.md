# X (Twitter) profile unofficial API: get a user's bio and followers

Automatically get a user's bio and followers on x.com. Look up an X (Twitter) user's profile by handle. Returns handle, user_id, name, bio, location, website, joined, followers_count, following_count, is_verified, is_self, is_following, follows_you. Counts are exact integers. bio and website carry the real destination URLs, with X's shortlinks resolved. is_following is null on your own profile. Any of is_self, is_following, follows_you and is_verified is null when X does not say. Requires being signed in to X; a missing or suspended account is an error that says which.

- Site: x.com
- Address: `reduck/x.com/get_user_info`
- Updated: 2026-10-16 (v13)
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
- `is_self` (boolean | null, required): True when this profile is the signed-in viewer's own; null when X does not say who the viewer is.
- `user_id` (string, required): Numeric rest_id.
- `follows_you` (boolean | null, required): Whether they follow you; null when X does not say.
- `is_verified` (boolean | null, required): Blue/verified badge; null when X does not say.
- `is_following` (boolean | null, required): Whether you follow them; null on your own profile or when X does not say.
- `bio` (string | null, optional): Profile bio text, with any t.co shortlinks replaced by their real destination (as the page displays them); null when empty.
- `joined` (string | null, optional): Account creation date in X's format, e.g. 'Tue Jun 02 20:12:29 +0000 2009'.
- `website` (string | null, optional): Expanded profile URL; null when the profile has none.
- `location` (string | null, optional): Profile location; null when empty.
- `followers_count` (integer | null, optional): Exact follower count as an integer.
- `following_count` (integer | null, optional): Exact count of accounts this profile follows; 0 is a real value.

## FAQ

### What does "X (Twitter) profile unofficial API: get a user's bio and followers" do?

Look up an X (Twitter) user's profile by handle. Returns handle, user_id, name, bio, location, website, joined, followers_count, following_count, is_verified, is_self, is_following, follows_you. Counts are exact integers. bio and website carry the real destination URLs, with X's shortlinks resolved. is_following is null on your own profile. Any of is_self, is_following, follows_you and is_verified is null when X does not say. Requires being signed in to X; a missing or suspended account is an error that says which.

### How do I automatically get a user's bio and followers on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_info

### Is there a x.com API to get a user's bio and followers?

You do not need one. "X (Twitter) profile unofficial API: get a user's bio and followers" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle.

### What does it return?

It returns bio, name, handle, joined, is_self, user_id, website, location, follows_you, is_verified, is_following, followers_count, following_count.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_user_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_user_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_user_info
