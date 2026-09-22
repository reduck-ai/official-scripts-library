# Get YC company profile

Automatically get YC company profile on ycombinator.com. Get one YC company's full public profile (ycombinator.com/companies/<slug>): pitch, batch/status, founders, socials, open jobs, news, launches, photos, founder Q&A.

- Site: ycombinator.com
- Address: `reduck/ycombinator.com/get_company`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ycombinator.com/get_company`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ycombinator.com/get_company
```

## Input

- `slug` (string, required): The company's YC slug — the last path segment of ycombinator.com/companies/<slug>, e.g. "airbnb". Same `slug` returned by search_companies.

## Output

- `id` (integer, required)
- `url` (string, required): Canonical YC page.
- `name` (string, required)
- `slug` (string, required)
- `qa` (array, optional): Founder/application Q&A as shown on the page (public answers only).
- `city` (string | null, optional)
- `jobs` (array, optional)
- `news` (array, optional)
- `tags` (array, optional)
- `batch` (string | null, optional)
- `links` (object, optional)
- `photos` (array, optional)
- `status` (string | null, optional): Active | Inactive | Acquired | Public.
- `videos` (object, optional)
- `country` (string | null, optional)
- `logoUrl` (string | null, optional): Stable public logo (presigned variants in props expire).
- `website` (string | null, optional)
- `founders` (array, optional)
- `launches` (array, optional)
- `location` (string | null, optional)
- `oneLiner` (string | null, optional)
- `teamSize` (integer | null, optional)
- `description` (string | null, optional)
- `yearFounded` (integer | null, optional)
- `primaryPartner` (object | null, optional)

## FAQ

### What does "Get YC company profile" do?

Get one YC company's full public profile (ycombinator.com/companies/<slug>): pitch, batch/status, founders, socials, open jobs, news, launches, photos, founder Q&A.

### How do I automatically get YC company profile on ycombinator.com?

Ask an AI agent connected to Reduck to run reduck/ycombinator.com/get_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ycombinator.com/get_company

### Is there a ycombinator.com API to get YC company profile?

You do not need one. "Get YC company profile" drives the real ycombinator.com pages in a browser, so it works whether or not ycombinator.com offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns id, qa, url, city, jobs, name, news, slug, tags, batch, links, photos, status, videos, country, logoUrl, website, founders, launches, location, oneLiner, teamSize, description, yearFounded, primaryPartner.

### Do I need to be logged in to ycombinator.com?

No. It only uses pages of ycombinator.com that are reachable without signing in.

### Does it change anything on ycombinator.com, or only read data?

Unknown: its author has not declared whether it changes anything on ycombinator.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ycombinator.com/get_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ycombinator.com/get_company

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ycombinator.com/get_company
