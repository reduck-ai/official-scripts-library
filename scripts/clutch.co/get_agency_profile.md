# Get Agency Profile (Clutch)

Automatically get Agency Profile (Clutch) on clutch.co. Reads a single agency's public Clutch profile: description, rating, price range, founding year, address, service offerings, certifications and recent client reviews.

- Site: clutch.co
- Address: `reduck/clutch.co/get_agency_profile`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/clutch.co/get_agency_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/clutch.co/get_agency_profile
```

## Input

- `slug` (string, required): The agency's Clutch profile slug, e.g. "ignite-visibility" (the segment after clutch.co/profile/ — found in search_agencies results' profileUrl).

## Output

- `name` (string | null, required)
- `slug` (string, required)
- `found` (boolean, required)
- `rating` (number | null, required)
- `address` (object | null, required)
- `reviews` (array, required)
- `services` (array, required)
- `telephone` (string | null, required)
- `priceRange` (string | null, required)
- `websiteUrl` (string | null, required)
- `description` (string | null, required)
- `reviewCount` (integer | null, required)
- `foundingYear` (integer | null, required)
- `certifications` (array, required)

## FAQ

### What does "Get Agency Profile (Clutch)" do?

Reads a single agency's public Clutch profile: description, rating, price range, founding year, address, service offerings, certifications and recent client reviews.

### How do I automatically get Agency Profile (Clutch) on clutch.co?

Ask an AI agent connected to Reduck to run reduck/clutch.co/get_agency_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/clutch.co/get_agency_profile

### Is there a clutch.co API to get Agency Profile (Clutch)?

You do not need one. "Get Agency Profile (Clutch)" drives the real clutch.co pages in a browser, so it works whether or not clutch.co offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns name, slug, found, rating, address, reviews, services, telephone, priceRange, websiteUrl, description, reviewCount, foundingYear, certifications.

### Do I need to be logged in to clutch.co?

No. It only uses pages of clutch.co that are reachable without signing in.

### Does it change anything on clutch.co, or only read data?

It only reads. It looks things up on clutch.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/clutch.co/get_agency_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/clutch.co/get_agency_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/clutch.co/get_agency_profile
