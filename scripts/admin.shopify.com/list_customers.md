# List Shopify store customers

Automatically list Shopify store customers on admin.shopify.com. Lists the customers of the signed-in Shopify store, most recently updated first, optionally narrowed by a free-text search (name, email and more, as the admin's customer search box takes it). Each customer comes with their name, email, phone, number of orders, amount spent, email marketing status, location and admin link. Returns one page of the admin's list at a time (50 customers); pass nextCursor back as cursor for the next page, and nextCursor is null on the last page. A search with no match returns an empty list. A signed-out browser fails with a sign-in error.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/list_customers`
- Updated: 2026-11-05 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/list_customers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_customers
```

## Input

- `query` (string, optional): Free-text search, as typed in the admin's customer search box (matches name, email, phone and more).
- `store` (string, optional): The store handle as it appears in the admin URL (admin.shopify.com/store/<handle>). Omit it to use the store the signed-in admin opens by default.
- `cursor` (string, optional): nextCursor from the previous page. Omit for the first page.

## Output

- `count` (integer, required)
- `store` (string, required)
- `total` (integer | null, required): How many customers match, as the admin counts them.
- `search` (string | null, required): The search the admin ran, or null when unfiltered.
- `hasMore` (boolean, required)
- `customers` (array, required)
- `nextCursor` (string | null, required): Pass as cursor to get the next page; null on the last page.

## FAQ

### What does "List Shopify store customers" do?

Lists the customers of the signed-in Shopify store, most recently updated first, optionally narrowed by a free-text search (name, email and more, as the admin's customer search box takes it). Each customer comes with their name, email, phone, number of orders, amount spent, email marketing status, location and admin link. Returns one page of the admin's list at a time (50 customers); pass nextCursor back as cursor for the next page, and nextCursor is null on the last page. A search with no match returns an empty list. A signed-out browser fails with a sign-in error.

### How do I automatically list Shopify store customers on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/list_customers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_customers

### Is there a admin.shopify.com API to list Shopify store customers?

You do not need one. "List Shopify store customers" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Optional: query, store, cursor.

### What does it return?

It returns count, store, total, search, hasMore, customers, nextCursor.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It only reads. It looks things up on admin.shopify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/list_customers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_customers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/list_customers
