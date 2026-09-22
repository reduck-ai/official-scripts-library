# Get LinkedIn profile

Automatically get LinkedIn profile on linkedin.com. Fetch a LinkedIn profile's top card and About section by publicId. Returns profileUrl, name, headline, degree, memberUrn, location, currentCompany, followers, connections, and about. Check name first: non-null means the record is trustworthy; null means the fetch failed. Requires being logged in to LinkedIn.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile`
- Updated: 2026-09-03 (v19)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile
```

## Input

- `publicId` (string, required): LinkedIn public profile id - the part after /in/ in the profile URL.

## Output

- `name` (string | null, required): The profile owner's name, and the response health check. Non-null means the top card parsed and the whole record is trustworthy. Null means the parse failed (auth wall, block, or blank render) — treat every other field as invalid rather than interpreting the nulls.
- `profileUrl` (string, required): Canonical profile URL.
- `about` (string | null, optional): Full About prose, line breaks preserved. Null means no About text was captured — either the profile has none, or (rarely) it did not load in time. Disambiguate with name: when name is non-null the top card parsed cleanly, so a null here almost always means the profile genuinely has no About section.
- `degree` (string | null, optional): Connection degree, normalised to "1st", "2nd" or "3rd" (with a trailing + when LinkedIn shows its 3rd-or-beyond badge) so it can be compared directly whatever language the page rendered in. Null on your own profile or when no badge is shown.
- `headline` (string | null, optional): Top-card headline line. Null when the profile has no headline.
- `location` (string | null, optional): Top-card location as rendered. Null when the profile exposes no contact link, which is the row it shares.
- `followers` (integer | null, optional): Top-card follower count as an integer, grouping separators removed. Null when the card shows no follower count.
- `memberUrn` (string | null, optional): Stable internal member id (an ACoAA… token, the tail of urn:li:fsd_profile:<id>). Unlike publicId it never changes, so it is the join key for search_people's connectionOf. Read from the profile card ids LinkedIn renders for the page, so it is present on every profile — including your own and members you are not connected to.
- `connections` (string | null, optional): Top-card connection count, canonicalised: the digits as a string (e.g. "25"), or "500+" for the capped value LinkedIn displays once a member passes 500. Null when the card shows no connection count.
- `currentCompany` (string | null, optional): Top-card current-employer chip. Null when the card surfaces no company chip — the employer is then only in get_profile_experience.

## FAQ

### What does "Get LinkedIn profile" do?

Fetch a LinkedIn profile's top card and About section by publicId. Returns profileUrl, name, headline, degree, memberUrn, location, currentCompany, followers, connections, and about. Check name first: non-null means the record is trustworthy; null means the fetch failed. Requires being logged in to LinkedIn.

### How do I automatically get LinkedIn profile on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile

### Is there a linkedin.com API to get LinkedIn profile?

You do not need one. "Get LinkedIn profile" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: publicId.

### What does it return?

It returns name, about, degree, headline, location, followers, memberUrn, profileUrl, connections, currentCompany.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile
