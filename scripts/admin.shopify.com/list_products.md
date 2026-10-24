# List Shopify store products

Automatically list Shopify store products on admin.shopify.com. Lists products from the signed-in Shopify admin, optionally filtered by tag, status or a free-text search, with each product's title, status, vendor, type, inventory, prices and link. Returns one page of the admin's list at a time (50 products, as the admin shows them); pass nextCursor back as cursor for the next page, and nextCursor is null on the last page. An empty list means no product matches. A signed-out browser fails with a sign-in error.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/list_products`
- Updated: 2026-10-23 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/list_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_products
```

## Input

- `tag` (string, optional): Only return products carrying this exact tag.
- `query` (string, optional): Free-text search, as typed in the admin's product search box (matches title, SKU, vendor and more). Shopify search syntax such as vendor:Acme or status:draft is also accepted.
- `store` (string, optional): The store handle as it appears in the admin URL (admin.shopify.com/store/<handle>). Omit it to use the store the signed-in admin opens by default.
- `cursor` (string, optional): nextCursor from the previous page. Omit for the first page.
- `status` (string, optional): Only return products with this status.

## Output

- `count` (integer, required)
- `store` (string, required)
- `search` (string | null, required): The search the admin ran, or null when unfiltered.
- `hasMore` (boolean, required): True when another page follows.
- `products` (array, required)
- `nextCursor` (string | null, required): Pass as cursor to get the next page; null on the last page.

## FAQ

### What does "List Shopify store products" do?

Lists products from the signed-in Shopify admin, optionally filtered by tag, status or a free-text search, with each product's title, status, vendor, type, inventory, prices and link. Returns one page of the admin's list at a time (50 products, as the admin shows them); pass nextCursor back as cursor for the next page, and nextCursor is null on the last page. An empty list means no product matches. A signed-out browser fails with a sign-in error.

### How do I automatically list Shopify store products on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/list_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_products

### Is there a admin.shopify.com API to list Shopify store products?

You do not need one. "List Shopify store products" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Optional: tag, query, store, cursor, status.

### What does it return?

It returns count, store, search, hasMore, products, nextCursor.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It only reads. It looks things up on admin.shopify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/list_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/list_products
