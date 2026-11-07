# Update Product Hunt profile (headline, about, links)

Automatically update Product Hunt profile (headline, about, links) on producthunt.com. Fill in the signed-in account's Product Hunt profile: the headline (short tagline under your name), the About text, and the additional links shown on the profile (LinkedIn, GitHub, X, a personal site...). Only the fields you pass are changed. Links are added next to the ones already on the profile; a link whose URL is already there is left as it is and listed in links_already_present. Returns the profile as Product Hunt holds it after saving, read back from the site. A signed-out browser fails with a signed-out error.

- Site: producthunt.com
- Address: `reduck/producthunt.com/update_profile`
- Updated: 2026-11-06 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/update_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/update_profile
```

## Input

- `about` (string, optional): Longer About text, line breaks allowed. Omit to keep the current one.
- `links` (array, optional): Links to add to the profile. Each has a display name and a full URL, e.g. {"name":"LinkedIn","url":"https://www.linkedin.com/in/username"}.
- `headline` (string, optional): Short tagline shown under your name, 40 characters at most (Product Hunt's limit), e.g. "Founding Engineer @ Reduck". Omit to keep the current one.

## Output

- `saved` (boolean, required): False when nothing needed changing, so nothing was sent.
- `username` (string, required)
- `name` (string | null, optional)
- `about` (string | null, optional)
- `links` (array, optional)
- `headline` (string | null, optional)
- `links_added` (array, optional)
- `profile_url` (string, optional)
- `links_already_present` (array, optional)

## FAQ

### What does "Update Product Hunt profile (headline, about, links)" do?

Fill in the signed-in account's Product Hunt profile: the headline (short tagline under your name), the About text, and the additional links shown on the profile (LinkedIn, GitHub, X, a personal site...). Only the fields you pass are changed. Links are added next to the ones already on the profile; a link whose URL is already there is left as it is and listed in links_already_present. Returns the profile as Product Hunt holds it after saving, read back from the site. A signed-out browser fails with a signed-out error.

### How do I automatically update Product Hunt profile (headline, about, links) on producthunt.com?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/update_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/update_profile

### Is there a producthunt.com API to update Product Hunt profile (headline, about, links)?

You do not need one. "Update Product Hunt profile (headline, about, links)" drives the real producthunt.com pages in a browser, so it works whether or not producthunt.com offers an API for this.

### What information do I need to provide?

Optional: about, links, headline.

### What does it return?

It returns name, about, links, saved, headline, username, links_added, profile_url, links_already_present.

### Do I need to be logged in to producthunt.com?

Yes. It acts as you on producthunt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the producthunt.com cookies saved by the Reduck extension.

### Does it change anything on producthunt.com, or only read data?

It makes changes on producthunt.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/update_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/update_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/update_profile
