# Get Instagram profile

Automatically get Instagram profile on instagram.com. You get the follower, following and post counts, bio, link and numeric user ID, exact when signed in.

- Site: instagram.com
- Address: `reduck/instagram.com/get_profile`
- Updated: 2026-10-05 (v6)
- Author: Reduck AI (reduck)

## About

Give it a handle such as natgeo and you get what the top of that profile shows (name, bio, the three counts, badges, category, link in bio) plus the numeric user_id that other Instagram scripts ask for. Say a small skincare brand has 40 creator handles from a hashtag. The team runs each one, keeps the accounts with 10,000 to 80,000 followers whose category mentions beauty, and only then pulls recent posts for the survivors before anyone gets a DM. Skip is_business in that filter, since it mirrors the business-account setting and there is no creator flag. Keep an eye on source too. With api, the data Instagram loads for a signed-in browser was captured and the counts are exact. With og_meta it was not, usually because the browser is logged out, so counts are rounded and bio, badges, category and link are null. A login wall makes the run fail, so sign in to Instagram there and retry.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_profile
```

## Input

- `username` (string, required): Handle without the @, e.g. 'natgeo'.

## Output

- `source` (string, required): api = exact data from Instagram's profile API (requires a session). og_meta = public page metadata fallback when logged out: counts are approximate (K/M/B rounded), unknown fields are null. A login-walled run is NOT returned as a result — it throws — so a null-filled payload can no longer be mistaken for a profile that hides its counts.
- `username` (string, required)
- `posts` (number | null, optional): Public post count; null on private/restricted views.
- `user_id` (string | null, optional): Stable numeric pk as a string; null when logged out and not embedded in the public page.
- `category` (string | null, optional)
- `biography` (string | null, optional): null in og fallback.
- `followers` (number | null, optional): Approximate (K/M/B rounded) in og fallback.
- `following` (number | null, optional)
- `full_name` (string | null, optional)
- `is_private` (boolean | null, optional): null when unknown (og fallback).
- `is_business` (boolean | null, optional): null when unknown (og fallback).
- `is_verified` (boolean | null, optional): null when unknown (og fallback).
- `external_url` (string | null, optional)
- `profile_pic_url` (string | null, optional)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "posts": 3.5,
  "source": "api",
  "user_id": "abc123",
  "category": "…",
  "username": "…",
  "biography": "…",
  "followers": 1200,
  "following": 3.5,
  "full_name": "…",
  "is_private": true,
  "is_business": true,
  "is_verified": true,
  "external_url": "https://example.com/item/123",
  "profile_pic_url": "https://example.com/item/123"
}
```

## FAQ

### What does "Get Instagram profile" do?

Get an Instagram profile by username. With a session: exact data from Instagram's profile API (source=api). Logged out, where Instagram still serves the profile publicly: falls back to the page's og metadata (source=og_meta) — counts are approximate (K/M/B rounded) and unknown fields (biography, is_verified, is_private, is_business, category, external_url) are null. When Instagram login-walls the profile instead, the run FAILS rather than returning an empty payload, so a walled run can never be mistaken for a profile that hides its counts. Returns source, username, user_id, full_name, biography, followers, following, posts, is_verified, is_private, is_business, category, external_url, and profile_pic_url.

### How do I automatically get Instagram profile on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_profile

### Is there a instagram.com API to get Instagram profile?

You do not need one. "Get Instagram profile" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns posts, source, user_id, category, username, biography, followers, following, full_name, is_private, is_business, is_verified, external_url, profile_pic_url.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I look up personal Instagram accounts, or only business and creator ones?

Personal accounts work, because the script reads the same profile header Instagram shows your signed-in browser. Meta's official route, Business Discovery, covers only professional (business or creator) accounts, skips age-gated ones and needs your own professional account linked through Facebook Login. Basic Display, Meta's API for connecting your own personal account to an app, was switched off on 4 December 2024.

### How do I find someone's Instagram user ID from their username?

Run get_profile with the handle and read user_id, the numeric account id Instagram uses internally, returned as a string. get_stories, get_highlights and get_tagged_posts take that id rather than the handle, while get_user_posts and get_user_reels take the username directly. When source is og_meta the id can come back null, so run it signed in whenever you need the id.

### Why are some follower counts round numbers like 1200000?

Round counts like 1200000 come from the logged-out fallback (source is og_meta), which reads the abbreviated numbers in the page preview, so 1.2M turns into 1200000, while counts written out in full such as 1,234 stay exact. The fallback only recognises the English words Followers, Following and Posts, so a preview served in another language gives null counts. With an Instagram session the profile API response is normally captured and source comes back as api with exact figures.

### What do I get for a private account?

Signed in, you get the header Instagram shows on a private account's locked profile: name, bio, follower and following counts, and is_private true, though posts can come back null on restricted views. Logged out, is_private is null, so the fallback cannot tell you the account is private. For the people behind those counts, get_followers returns only a capped preview unless you follow the account.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_profile
