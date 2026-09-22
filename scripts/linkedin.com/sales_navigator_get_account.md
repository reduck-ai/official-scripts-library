# Sales Navigator: get account

Automatically get account on linkedin.com. Fetch a LinkedIn Sales Navigator company account by its numeric Sales Navigator id (from search_accounts, or a companyUrn on search_people). Needs a Sales Navigator seat; headcount history and median tenure are null when no insights panel is present. Returns name, description, industry, type, specialties, website, year founded, headquarters and location, revenue range, employee count and growth, headcount history, median tenure, and spotlight employees (name plus leadId to pivot to get_lead).

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_get_account`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_get_account`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_account
```

## Input

- `accountId` (string | integer, required): Numeric Sales Navigator company id (e.g. 1066442 for Datadog). Sourced from sales_navigator_search_accounts (accountId) or search_people (companyUrn urn:li:fs_salesCompany:N).

## Output

- `name` (string, required)
- `accountId` (string, required)
- `type` (string | null, optional): Company type (Public Company, Privately Held, ...).
- `saved` (boolean, optional)
- `starred` (boolean, optional)
- `website` (string | null, optional)
- `industry` (string | null, optional)
- `location` (string | null, optional)
- `employees` (array, optional): Spotlight employees surfaced on the company page (name + leadId to pivot to get_lead).
- `listCount` (integer | null, optional)
- `description` (string | null, optional)
- `specialties` (array, optional)
- `yearFounded` (integer | null, optional)
- `headquarters` (object | null, optional): Structured HQ address (country, geographicArea, city, postalCode, line1, line2).
- `revenueRange` (string | null, optional): Estimated revenue range, e.g. "500M-1B USD".
- `employeeCount` (integer | null, optional): Latest LinkedIn-tracked headcount (from the insights time series); null if no insights panel.
- `salesAccountUrl` (string, optional)
- `headcountHistory` (array, optional): Monthly headcount time series; empty when no insights panel.
- `employeeGrowthPct` (object, optional): Headcount growth % keyed by timespan (SIX_MONTHS / YEAR / TWO_YEAR).
- `medianTenureYears` (number | null, optional)
- `flagshipCompanyUrl` (string | null, optional): Classic linkedin.com/company/ URL.

## FAQ

### What does "Sales Navigator: get account" do?

Fetch a LinkedIn Sales Navigator company account by its numeric Sales Navigator id (from search_accounts, or a companyUrn on search_people). Needs a Sales Navigator seat; headcount history and median tenure are null when no insights panel is present. Returns name, description, industry, type, specialties, website, year founded, headquarters and location, revenue range, employee count and growth, headcount history, median tenure, and spotlight employees (name plus leadId to pivot to get_lead).

### How do I automatically get account on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_account, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_account

### Is there a linkedin.com API to get account?

You do not need one. "Sales Navigator: get account" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: accountId.

### What does it return?

It returns name, type, saved, starred, website, industry, location, accountId, employees, listCount, description, specialties, yearFounded, headquarters, revenueRange, employeeCount, salesAccountUrl, headcountHistory, employeeGrowthPct, medianTenureYears, flagshipCompanyUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_account, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_account

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_get_account
