# Get Leboncoin seller profile

Automatically get Leboncoin seller profile on leboncoin.fr. Fetch a Leboncoin seller's public profile by its URL (as returned by get_ad's seller_profile_url). Works for both professional stores and private-individual sellers, returning a unified shape: name, member-since date, total ad count, response rate/time, presence, badges, and description. Pro sellers additionally get address, opening hours, website, and an aggregated rating with sample reviews — these are null for private sellers, who have no storefront or public rating on the site.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/get_seller_profile`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/get_seller_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/get_seller_profile
```

## Input

- `url` (string, required): Seller profile URL, e.g. 'https://www.leboncoin.fr/boutique/1397746/store.htm' (pro) or 'https://www.leboncoin.fr/profile/<user_id>/offers' (private) — as returned by get_ad's seller_profile_url field.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `seller_type` (string, required)
- `city` (string | null, optional)
- `badges` (array, optional)
- `address` (string | null, optional)
- `zipcode` (string | null, optional)
- `logo_url` (string | null, optional)
- `total_ads` (integer | null, optional)
- `description` (string | null, optional)
- `website_url` (string | null, optional)
- `member_since` (string | null, optional)
- `rating_count` (integer | null, optional)
- `rating_value` (number | null, optional)
- `opening_hours` (string | null, optional)
- `presence_text` (string | null, optional)
- `rating_source` (string | null, optional)
- `response_rate` (number | null, optional)
- `response_time_text` (string | null, optional)

## FAQ

### What does "Get Leboncoin seller profile" do?

Fetch a Leboncoin seller's public profile by its URL (as returned by get_ad's seller_profile_url). Works for both professional stores and private-individual sellers, returning a unified shape: name, member-since date, total ad count, response rate/time, presence, badges, and description. Pro sellers additionally get address, opening hours, website, and an aggregated rating with sample reviews — these are null for private sellers, who have no storefront or public rating on the site.

### How do I automatically get Leboncoin seller profile on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/get_seller_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/get_seller_profile

### Is there a leboncoin.fr API to get Leboncoin seller profile?

You do not need one. "Get Leboncoin seller profile" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, city, name, badges, address, zipcode, logo_url, total_ads, description, seller_type, website_url, member_since, rating_count, rating_value, opening_hours, presence_text, rating_source, response_rate, response_time_text.

### Do I need to be logged in to leboncoin.fr?

No. It only uses pages of leboncoin.fr that are reachable without signing in.

### Does it change anything on leboncoin.fr, or only read data?

It only reads. It looks things up on leboncoin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/get_seller_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/get_seller_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/get_seller_profile
