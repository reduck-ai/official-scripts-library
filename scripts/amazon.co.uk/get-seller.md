# Get Amazon.co.uk seller profile and feedback

Automatically get Amazon.co.uk seller profile and feedback on amazon.co.uk. Look up an Amazon.co.uk marketplace seller by seller ID: display name, storefront, description, customer service phone, registered business details, and feedback by period (30 days, 90 days, 12 months, lifetime) with the 12-month positive percentage.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/get-seller`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/get-seller`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get-seller
```

## Input

- `sellerId` (string, required): Amazon seller ID, from the Sold by link of a product or a storefront URL (me= or seller=).

## Output

- `url` (string, required)
- `seller_id` (string, required)
- `seller_name` (string | null, required): Display name; null when the seller page does not show one.
- `about` (string | null, optional)
- `feedback` (object, optional)
- `logo_url` (string | null, optional)
- `storefront_url` (string | null, optional)
- `business_details` (array, optional)
- `positive_percent_12m` (integer | null, optional)
- `customer_service_phone` (string | null, optional)

## FAQ

### What does "Get Amazon.co.uk seller profile and feedback" do?

Look up an Amazon.co.uk marketplace seller by seller ID: display name, storefront, description, customer service phone, registered business details, and feedback by period (30 days, 90 days, 12 months, lifetime) with the 12-month positive percentage.

### How do I automatically get Amazon.co.uk seller profile and feedback on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/get-seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get-seller

### Is there a amazon.co.uk API to get Amazon.co.uk seller profile and feedback?

You do not need one. "Get Amazon.co.uk seller profile and feedback" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Required: sellerId.

### What does it return?

It returns url, about, feedback, logo_url, seller_id, seller_name, storefront_url, business_details, positive_percent_12m, customer_service_phone.

### Do I need to be logged in to amazon.co.uk?

No. It only uses pages of amazon.co.uk that are reachable without signing in.

### Does it change anything on amazon.co.uk, or only read data?

It only reads. It looks things up on amazon.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/get-seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get-seller

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/get-seller
