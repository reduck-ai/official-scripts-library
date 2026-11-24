# Request Amazon review access

Automatically request Amazon review access on amazon.com. When Amazon limits review access for your Amazon.com account after it detects unusual activity, its reviews pages show only the top reviews, with no filters and no paging. This sends Amazon's own request to verify the account and restore full access, from a product's reviews page. Amazon answers by email, within 3 days. Returns the access the page shows: full (nothing to request), limited, or limited_request_sent, with Amazon's message, and whether this run sent the request. A request already sent is not sent again. Get Amazon product reviews reports the same access in its result.

- Site: amazon.com
- Address: `reduck/amazon.com/request_review_access`
- Updated: 2026-11-23 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/request_review_access`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/request_review_access
```

## Input

- `asin` (string, required): ASIN of a product that has reviews, for example the one Get Amazon product reviews could not filter. Amazon shows the request on every reviews page of a limited account, so any product with reviews works.

## Output

- `asin` (string, required)
- `sent` (boolean, required): True when this run sent the request and Amazon accepted it.
- `access` (string, required): Review access as the reviews page shows it after the run. full: no limit, nothing to request. limited: the limit is on and no request is pending. limited_request_sent: a request is pending until Amazon answers by email.
- `message` (string | null, required): Amazon's message about the limit or the request, as the page shows it, in the page's language. Null when access is full.

## FAQ

### What does "Request Amazon review access" do?

When Amazon limits review access for your Amazon.com account after it detects unusual activity, its reviews pages show only the top reviews, with no filters and no paging. This sends Amazon's own request to verify the account and restore full access, from a product's reviews page. Amazon answers by email, within 3 days. Returns the access the page shows: full (nothing to request), limited, or limited_request_sent, with Amazon's message, and whether this run sent the request. A request already sent is not sent again. Get Amazon product reviews reports the same access in its result.

### How do I automatically request Amazon review access on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/request_review_access, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/request_review_access

### Is there a amazon.com API to request Amazon review access?

You do not need one. "Request Amazon review access" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Required: asin.

### What does it return?

It returns asin, sent, access, message.

### Do I need to be logged in to amazon.com?

Yes. It acts as you on amazon.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.com cookies saved by the Reduck extension.

### Does it change anything on amazon.com, or only read data?

It makes changes on amazon.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/request_review_access, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/request_review_access

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/request_review_access
