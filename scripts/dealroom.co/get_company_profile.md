# Dealroom: Get Company Profile

Automatically get Company Profile on dealroom.co. Fetch a company's full Dealroom profile by its Dealroom path/slug (as returned by the Search Companies script) — overview, HQ, funding rounds, investors, valuation, industries, technologies and social links.

- Site: dealroom.co
- Address: `reduck/dealroom.co/get_company_profile`
- Updated: 2026-08-19 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dealroom.co/get_company_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dealroom.co/get_company_profile
```

## Input

- `path` (string, required): Dealroom company path/slug, e.g. "revolut" (from a Dealroom company URL like dealroom.co/companies/revolut, or from Search Companies results).

## Output

- `path` (string | null, required)
- `name` (string | null, optional)
- `tags` (array, optional)
- `type` (string | null, optional)
- `uuid` (string | null, optional)
- `about` (string | null, optional)
- `tagline` (string | null, optional)
- `employees` (string | null, optional)
- `investors` (array, optional)
- `hqLocation` (object | null, optional)
- `industries` (array, optional)
- `launchYear` (integer | null, optional)
- `twitterUrl` (string | null, optional)
- `websiteUrl` (string | null, optional)
- `growthStage` (string | null, optional)
- `launchMonth` (integer | null, optional)
- `linkedinUrl` (string | null, optional)
- `technologies` (array, optional)
- `totalFunding` (object | null, optional)
- `careerPageUrl` (string | null, optional)
- `companyStatus` (string | null, optional)
- `fundingRounds` (array, optional)
- `employeesLatest` (integer | null, optional)
- `latestValuation` (object | null, optional)

## FAQ

### What does "Dealroom: Get Company Profile" do?

Fetch a company's full Dealroom profile by its Dealroom path/slug (as returned by the Search Companies script) — overview, HQ, funding rounds, investors, valuation, industries, technologies and social links.

### How do I automatically get Company Profile on dealroom.co?

Ask an AI agent connected to Reduck to run reduck/dealroom.co/get_company_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dealroom.co/get_company_profile

### Is there a dealroom.co API to get Company Profile?

You do not need one. "Dealroom: Get Company Profile" drives the real dealroom.co pages in a browser, so it works whether or not dealroom.co offers an API for this.

### What information do I need to provide?

Required: path.

### What does it return?

It returns name, path, tags, type, uuid, about, tagline, employees, investors, hqLocation, industries, launchYear, twitterUrl, websiteUrl, growthStage, launchMonth, linkedinUrl, technologies, totalFunding, careerPageUrl, companyStatus, fundingRounds, employeesLatest, latestValuation.

### Do I need to be logged in to dealroom.co?

Yes. It acts as you on dealroom.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dealroom.co cookies saved by the Reduck extension.

### Does it change anything on dealroom.co, or only read data?

It only reads. It looks things up on dealroom.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dealroom.co/get_company_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dealroom.co/get_company_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dealroom.co/get_company_profile
