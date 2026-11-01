# Get Amazon.de seller profile and feedback

Automatically get Amazon.de seller profile and feedback on amazon.de. Look up an Amazon.de marketplace seller by its seller ID and get the public profile: the seller's display name, logo, storefront link, self-written description, customer service phone, and the registered business name and address. You also get their feedback record broken out by period — star rating and number of ratings over the last 30 days, 90 days, 12 months and lifetime — plus the headline percentage of positive feedback. Useful for judging who you would actually be buying from before ordering.

- Site: amazon.de
- Address: `reduck/amazon.de/get-seller`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.de/get-seller`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.de/get-seller
```

## Input

- `sellerId` (string, required): Amazon seller ID, e.g. A294P4X9EWVXLJ. It appears in a product's "Sold by" link and in storefront URLs as the me= or seller= value.

## Output

- `url` (string, required)
- `seller_id` (string, required)
- `seller_name` (string, required)
- `about` (string | null, optional)
- `feedback` (object, optional)
- `logo_url` (string | null, optional)
- `storefront_url` (string | null, optional)
- `business_details` (array, optional)
- `positive_percent_12m` (integer | null, optional)
- `customer_service_phone` (string | null, optional)

## FAQ

### What does "Get Amazon.de seller profile and feedback" do?

Look up an Amazon.de marketplace seller by its seller ID and get the public profile: the seller's display name, logo, storefront link, self-written description, customer service phone, and the registered business name and address. You also get their feedback record broken out by period — star rating and number of ratings over the last 30 days, 90 days, 12 months and lifetime — plus the headline percentage of positive feedback. Useful for judging who you would actually be buying from before ordering.

### How do I automatically get Amazon.de seller profile and feedback on amazon.de?

Ask an AI agent connected to Reduck to run reduck/amazon.de/get-seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/get-seller

### Is there a amazon.de API to get Amazon.de seller profile and feedback?

You do not need one. "Get Amazon.de seller profile and feedback" drives the real amazon.de pages in a browser, so it works whether or not amazon.de offers an API for this.

### What information do I need to provide?

Required: sellerId.

### What does it return?

It returns url, about, feedback, logo_url, seller_id, seller_name, storefront_url, business_details, positive_percent_12m, customer_service_phone.

### Do I need to be logged in to amazon.de?

No. It only uses pages of amazon.de that are reachable without signing in.

### Does it change anything on amazon.de, or only read data?

It only reads. It looks things up on amazon.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.de/get-seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/get-seller

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.de/get-seller
