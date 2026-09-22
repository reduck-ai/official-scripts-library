# Get LinkedIn company info

Automatically get LinkedIn company info on linkedin.com. Get a LinkedIn company's full profile from its URL or bare slug. employeeCount is LinkedIn members associated with the page, not declared size, and can wildly exceed employeeCountRange; use employeeCountRange for self-declared size. websiteUrl is verbatim and can be a linkedin.com self-link. Returns companyId, universalName, name, tagline, description, websiteUrl, industries, specialities, employeeCount, employeeCountRange, followerCount, foundedYear, phone, headquarters, locations, and logoUrl.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_company_info`
- Updated: 2026-09-03 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_company_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_info
```

## Input

- `url` (string, optional): LinkedIn company page URL (e.g. https://www.linkedin.com/company/almapay/), a bare slug (e.g. almapay), or the numeric company id.
- `slug` (string, optional): Alias for url — accepted for compatibility; prefer url.
- `company` (string, optional): Alias for url — accepted for compatibility; prefer url.
- `companySlug` (string, optional): Alias for url — accepted for compatibility; prefer url.
- `companyUrlOrSlug` (string, optional): Alias for url — accepted for compatibility; prefer url.

## Output

- `name` (string, required)
- `companyId` (string, required): Inner numeric LinkedIn company ID from urn:li:fsd_company:N (e.g. 18834371 for almapay). Stable join key, and accepted as input in place of the slug.
- `universalName` (string, required): Canonical slug as LinkedIn returns it — may differ from the requested one if the page was renamed or redirected, which is why it is worth reading back rather than assuming the slug you asked for.
- `phone` (string | null, optional)
- `logoUrl` (string | null, optional)
- `tagline` (string | null, optional)
- `locations` (array, optional)
- `industries` (array, optional)
- `websiteUrl` (string | null, optional): Company-declared website, returned verbatim — can be a linkedin.com self-link when the company set its own LinkedIn page as website (seen on stealth pages). Not normalized; filter linkedin.com values downstream if you need a real external site.
- `description` (string | null, optional)
- `foundedYear` (integer | null, optional)
- `linkedinUrl` (string | null, optional)
- `headquarters` (object | null, optional)
- `specialities` (array, optional)
- `employeeCount` (integer | null, optional): Count of LinkedIn members associated with the page, not the declared size — on catch-all/stealth pages it can wildly exceed employeeCountRange (battle-tested: 5,933 members on a page declaring 2-10). Use employeeCountRange for the company's self-declared size.
- `followerCount` (integer | null, optional)
- `employeeCountRange` (object | null, optional)

## FAQ

### What does "Get LinkedIn company info" do?

Get a LinkedIn company's full profile from its URL or bare slug. employeeCount is LinkedIn members associated with the page, not declared size, and can wildly exceed employeeCountRange; use employeeCountRange for self-declared size. websiteUrl is verbatim and can be a linkedin.com self-link. Returns companyId, universalName, name, tagline, description, websiteUrl, industries, specialities, employeeCount, employeeCountRange, followerCount, foundedYear, phone, headquarters, locations, and logoUrl.

### How do I automatically get LinkedIn company info on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_info

### Is there a linkedin.com API to get LinkedIn company info?

You do not need one. "Get LinkedIn company info" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: url, slug, company, companySlug, companyUrlOrSlug.

### What does it return?

It returns name, phone, logoUrl, tagline, companyId, locations, industries, websiteUrl, description, foundedYear, linkedinUrl, headquarters, specialities, employeeCount, followerCount, universalName, employeeCountRange.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_company_info
