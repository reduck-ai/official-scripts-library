# Get LinkedIn profile photo

Automatically get LinkedIn profile photo on linkedin.com. Get a LinkedIn profile's avatar (profile photo) image link by publicId. Returns profileUrl, name, photoUrl (a signed image link: keep its query string, which is required to fetch the image), photoAlt, and hasPhoto (false when the profile shows only the default ghost avatar). Accepts a vanity slug, the obfuscated member token, or a full profile URL. Complements get_profile, which returns everything except the photo. Until 19 Oct 2026 a publicIds list was accepted; a call still sending it fails with a message saying to send one publicId per call.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_photo`
- Updated: 2026-10-22 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_photo`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_photo
```

## Input

- `publicId` (string, optional): LinkedIn public profile id — the /in/ segment. Accepts the vanity slug (e.g. 'dhuynh95'), the obfuscated member token (ACoAA…), or a full profile URL (the /in/<id> is extracted).
- `publicIds` (array, optional): Not supported since 19 Oct 2026: the run fails with a message saying so. Send one publicId per call and fan out with run_script's scripts.

## Output

- `name` (string, required): Profile name. Never null: a profile whose name cannot be read fails instead.
- `hasPhoto` (boolean, required): True when a real display photo was found; false when the profile shows only LinkedIn's default ghost avatar.
- `photoUrl` (string | null, required): Full signed link to the photo. Its query string is part of the signature, so keep it as given. Null when the profile has no real photo.
- `profileUrl` (string, required)
- `photoAlt` (string | null, optional): The photo's alt text; null if absent.

## FAQ

### What does "Get LinkedIn profile photo" do?

Get a LinkedIn profile's avatar (profile photo) image link by publicId. Returns profileUrl, name, photoUrl (a signed image link: keep its query string, which is required to fetch the image), photoAlt, and hasPhoto (false when the profile shows only the default ghost avatar). Accepts a vanity slug, the obfuscated member token, or a full profile URL. Complements get_profile, which returns everything except the photo. Until 19 Oct 2026 a publicIds list was accepted; a call still sending it fails with a message saying to send one publicId per call.

### How do I automatically get LinkedIn profile photo on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_photo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_photo

### Is there a linkedin.com API to get LinkedIn profile photo?

You do not need one. "Get LinkedIn profile photo" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: publicId, publicIds.

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
