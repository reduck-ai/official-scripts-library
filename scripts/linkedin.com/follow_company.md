# Follow LinkedIn company

Automatically follow LinkedIn company on linkedin.com. Follow a LinkedIn company page by URL or bare slug. Safe to repeat: it returns already_following if you already follow it, and not_found when the page doesn't exist. Also returns the company's numeric id, canonical slug, and display name.

- Site: linkedin.com
- Address: `reduck/linkedin.com/follow_company`
- Updated: 2026-09-03 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/follow_company`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/follow_company
```

## Input

- `url` (string, optional): LinkedIn company page URL (e.g. https://www.linkedin.com/company/almapay/) or bare slug (e.g. almapay). A /showcase/<slug>/ URL also works.
- `slug` (string, optional): Alias for url — accepted for compatibility; prefer url.
- `company` (string, optional): Alias for url — accepted for compatibility; prefer url.
- `companySlug` (string, optional): Alias for url — accepted for compatibility; prefer url.
- `companyUrlOrSlug` (string, optional): Alias for url — accepted for compatibility; prefer url.

## Output

- `status` (string, required): followed = just followed; already_following = the page already showed you follow it; not_found = the company page doesn't exist.
- `companyUrl` (string, required)
- `name` (string | null, optional): Company display name (h1). Null only when not_found.
- `companyId` (string | null, optional): Numeric LinkedIn company id, resolved from the SSR hydration blob's entityUrn nearest the current universalName. Null only when not_found or the blob wasn't found.
- `universalName` (string | null, optional): Canonical slug segment from the resolved page URL (company or showcase page). Null only when not_found.

## FAQ

### What does "Follow LinkedIn company" do?

Follow a LinkedIn company page by URL or bare slug. Safe to repeat: it returns already_following if you already follow it, and not_found when the page doesn't exist. Also returns the company's numeric id, canonical slug, and display name.

### How do I automatically follow LinkedIn company on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/follow_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/follow_company

### Is there a linkedin.com API to follow LinkedIn company?

You do not need one. "Follow LinkedIn company" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: url, slug, company, companySlug, companyUrlOrSlug.

### What does it return?

It returns name, status, companyId, companyUrl, universalName.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/follow_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/follow_company

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/follow_company
