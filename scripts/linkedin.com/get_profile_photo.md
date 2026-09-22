# Get LinkedIn profile photo

Automatically get LinkedIn profile photo on linkedin.com. Get a LinkedIn profile's avatar (profile photo) image URL by publicId. Returns profileUrl, name, photoUrl (the signed media.licdn.com display-photo URL — keep its query string, it is required to fetch the image), photoAlt, and hasPhoto (false when the profile shows only the default ghost avatar). Accepts a vanity slug, the obfuscated ACoAA… member token, or a full /in/ URL. Complements get_profile, which returns everything except the photo.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_photo`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_photo`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_photo
```

## Input

- `publicId` (string, required): LinkedIn public profile id — the /in/ segment. Accepts the vanity slug (e.g. 'dhuynh95'), the obfuscated member token (ACoAA…), or a full profile URL (the /in/<id> is extracted).

## Output

- `name` (string, required): Profile name (first main h2). Never null: a top-card that does not parse (auth wall, class rotation, blank shell) throws instead of returning a nameless record.
- `hasPhoto` (boolean, required): True when a real display photo was found; false when the profile shows only LinkedIn's default ghost avatar.
- `photoUrl` (string | null, required): Full signed avatar URL on media.licdn.com (…/profile-displayphoto-…). The ?e=&v=&t= query string is part of the signature — do NOT strip it or the fetch 403s. Null when the profile has no real photo.
- `profileUrl` (string, required)
- `photoAlt` (string | null, optional): The avatar img alt text; null if absent — LinkedIn currently renders the avatar with an empty alt.

## FAQ

### What does "Get LinkedIn profile photo" do?

Get a LinkedIn profile's avatar (profile photo) image URL by publicId. Returns profileUrl, name, photoUrl (the signed media.licdn.com display-photo URL — keep its query string, it is required to fetch the image), photoAlt, and hasPhoto (false when the profile shows only the default ghost avatar). Accepts a vanity slug, the obfuscated ACoAA… member token, or a full /in/ URL. Complements get_profile, which returns everything except the photo.

### How do I automatically get LinkedIn profile photo on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_photo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_photo

### Is there a linkedin.com API to get LinkedIn profile photo?

You do not need one. "Get LinkedIn profile photo" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: publicId.

### What does it return?

It returns name, hasPhoto, photoAlt, photoUrl, profileUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_photo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_photo

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile_photo
