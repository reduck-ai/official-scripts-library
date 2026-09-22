# Get Trustpilot company profile

Automatically get Trustpilot company profile on trustpilot.com. Get a Trustpilot company profile: TrustScore, stars, review count, full 1-5 star rating distribution, categories, breadcrumb, contact info, claim status and reply behavior. Input is the domain key (e.g. "amazon.com"); the resolved identifyingName is returned (may differ via redirect).

- Site: trustpilot.com
- Address: `reduck/trustpilot.com/get_company`
- Updated: 2026-08-14 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trustpilot.com/get_company`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_company
```

## Input

- `domain` (string, required): Company domain key, e.g. "amazon.com" or "www.nike.com" (the identifyingName from search_company).

## Output

- `id` (string, required)
- `stars` (number | null, required)
- `domain` (string, required): Resolved identifyingName (may differ from the requested input after redirect).
- `trustScore` (number | null, required)
- `displayName` (string, required)
- `numberOfReviews` (integer | null, required)
- `ratingDistribution` (object, required)
- `isClosed` (boolean | null, optional)
- `isClaimed` (boolean | null, optional)
- `breadcrumb` (object | null, optional)
- `categories` (array, optional)
- `websiteUrl` (string | null, optional)
- `contactInfo` (object | null, optional)
- `verification` (object | null, optional)
- `replyBehavior` (object | null, optional)
- `numberOfReviewsLast12Months` (integer | null, optional)

## FAQ

### What does "Get Trustpilot company profile" do?

Get a Trustpilot company profile: TrustScore, stars, review count, full 1-5 star rating distribution, categories, breadcrumb, contact info, claim status and reply behavior. Input is the domain key (e.g. "amazon.com"); the resolved identifyingName is returned (may differ via redirect).

### How do I automatically get Trustpilot company profile on trustpilot.com?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_company

### Is there a trustpilot.com API to get Trustpilot company profile?

You do not need one. "Get Trustpilot company profile" drives the real trustpilot.com pages in a browser, so it works whether or not trustpilot.com offers an API for this.

### What information do I need to provide?

Required: domain.

### What does it return?

It returns id, stars, domain, isClosed, isClaimed, breadcrumb, categories, trustScore, websiteUrl, contactInfo, displayName, verification, replyBehavior, numberOfReviews, ratingDistribution, numberOfReviewsLast12Months.

### Do I need to be logged in to trustpilot.com?

No. It only uses pages of trustpilot.com that are reachable without signing in.

### Does it change anything on trustpilot.com, or only read data?

It only reads. It looks things up on trustpilot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_company

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trustpilot.com/get_company
