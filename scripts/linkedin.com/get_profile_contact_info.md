# Get LinkedIn profile contact info

Automatically get LinkedIn profile contact info on linkedin.com. Get a LinkedIn profile's Contact info overlay (profile link, email, phone, address, birthday, websites, social handles - whichever the profile exposes) by public ID. get_profile stops at the top card and About section; this reaches the separate Contact info panel. Requires being logged in to LinkedIn.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_contact_info`
- Updated: 2026-09-03 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_contact_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_contact_info
```

## Input

- `publicId` (string, required): LinkedIn public profile id - the part after /in/ in the profile URL. Accepts the vanity slug (e.g. 'williamhgates') or the obfuscated member token (ACoAA...); both resolve.

## Output

- `email` (string | null, required): Email address, when the profile exposes one.
- `fields` (array, required): Every row shown in the panel verbatim (profile/email/websites included), for fields not promoted to a named property above - phone, address, birthday, connected-on date, social handles, etc. Empty when hasContactInfo is false.
- `websites` (array, required): Website links the profile lists (a profile can list more than one, each with its own label like 'Company' or 'Blog').
- `profileUrl` (string | null, required): This profile's own canonical URL, from the panel's own 'profile' row (always present when hasContactInfo is true).
- `hasContactInfo` (boolean, required): False when the profile offers no Contact info link at all (privacy setting, or the viewer lacks access) - every other field is then null/empty rather than a parse failure.

## FAQ

### What does "Get LinkedIn profile contact info" do?

Get a LinkedIn profile's Contact info overlay (profile link, email, phone, address, birthday, websites, social handles - whichever the profile exposes) by public ID. get_profile stops at the top card and About section; this reaches the separate Contact info panel. Requires being logged in to LinkedIn.

### How do I automatically get LinkedIn profile contact info on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_contact_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_contact_info

### Is there a linkedin.com API to get LinkedIn profile contact info?

You do not need one. "Get LinkedIn profile contact info" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: publicId.

### What does it return?

It returns email, fields, websites, profileUrl, hasContactInfo.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_contact_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_contact_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile_contact_info
