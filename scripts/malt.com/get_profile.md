# Get Malt freelancer profile

Automatically get Malt freelancer profile on malt.com. Fetches a Malt freelancer's full public profile by seoAlias (the slug from search_freelancers' profileUrl, e.g. "samuelguetta"). Returns bio, address, availability, price, languages, category, experiences, educations, certifications and visible client reviews. Languages/categories are sometimes omitted by Malt's own page even for real profiles (page-state variance), so treat empty as a legitimate result, not an error.

- Site: malt.com
- Address: `reduck/malt.com/get_profile`
- Updated: 2026-08-26 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/malt.com/get_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/malt.com/get_profile
```

## Input

- `seoAlias` (string, required): Profile slug, e.g. "samuelguetta" (from a search_freelancers result's profileUrl: /profile/<seoAlias>)

## Output

- `id` (string | null, optional): Mongo-style profile id matching search_freelancers' id field
- `badge` (string | null, optional)
- `price` (object, optional)
- `address` (object | null, optional)
- `headline` (string | null, optional)
- `lastname` (string | null, optional)
- `seoAlias` (string | null, optional)
- `firstname` (string | null, optional)
- `languages` (array, optional)
- `categories` (object, optional)
- `educations` (array, optional)
- `reputation` (object, optional)
- `description` (string | null, optional)
- `experiences` (array, optional)
- `availability` (object | null, optional)
- `certifications` (array, optional)
- `experienceLevel` (string | null, optional)

## FAQ

### What does "Get Malt freelancer profile" do?

Fetches a Malt freelancer's full public profile by seoAlias (the slug from search_freelancers' profileUrl, e.g. "samuelguetta"). Returns bio, address, availability, price, languages, category, experiences, educations, certifications and visible client reviews. Languages/categories are sometimes omitted by Malt's own page even for real profiles (page-state variance), so treat empty as a legitimate result, not an error.

### How do I automatically get Malt freelancer profile on malt.com?

Ask an AI agent connected to Reduck to run reduck/malt.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/malt.com/get_profile

### Is there a malt.com API to get Malt freelancer profile?

You do not need one. "Get Malt freelancer profile" drives the real malt.com pages in a browser, so it works whether or not malt.com offers an API for this.

### What information do I need to provide?

Required: seoAlias.

### What does it return?

It returns id, badge, price, address, headline, lastname, seoAlias, firstname, languages, categories, educations, reputation, description, experiences, availability, certifications, experienceLevel.

### Do I need to be logged in to malt.com?

No. It only uses pages of malt.com that are reachable without signing in.

### Does it change anything on malt.com, or only read data?

It only reads. It looks things up on malt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/malt.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/malt.com/get_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/malt.com/get_profile
