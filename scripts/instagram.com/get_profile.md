# Get Instagram profile

Automatically get Instagram profile on instagram.com. Get an Instagram profile by username. With a session: exact data from Instagram's profile API (source=api). Logged out, where Instagram still serves the profile publicly: falls back to the page's og metadata (source=og_meta) — counts are approximate (K/M/B rounded) and unknown fields (biography, is_verified, is_private, is_business, category, external_url) are null. When Instagram login-walls the profile instead, the run FAILS rather than returning an empty payload, so a walled run can never be mistaken for a profile that hides its counts. Returns source, username, user_id, full_name, biography, followers, following, posts, is_verified, is_private, is_business, category, external_url, and profile_pic_url.

- Site: instagram.com
- Address: `reduck/instagram.com/get_profile`
- Updated: 2026-09-14 (v6)
- Author: Reduck AI (reduck)

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

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_profile
