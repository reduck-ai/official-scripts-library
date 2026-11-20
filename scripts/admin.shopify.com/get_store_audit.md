# Audit a Shopify store

Reads the health data of the signed-in Shopify store: its name, domain, plan and currency; how many products it has by status, how many orders in the last 30 days and how many customers; and one page of products, most recently updated first, with whether each has an image, the length of its description, its lowest price and its stock. Use these fields to spot catalogue problems such as missing images, empty descriptions, zero prices or active products out of stock. Pass nextCursor back as cursor for the next page. Read-only.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/get_store_audit`
- Updated: 2026-11-19 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/get_store_audit`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/get_store_audit
```

## Input

- `limit` (integer, optional): How many products to return in this page, most recently updated first.
- `store` (string, optional): The store handle as it appears in the admin URL. Omit it to use the store the signed-in admin opens by default.
- `cursor` (string, optional): The nextCursor from a previous call, to get the next page of products. Omit for the first page.

## Output

- `shop` (object, required)
- `count` (integer, required)
- `store` (string, required)
- `counts` (object, required)
- `hasMore` (boolean, required)
- `products` (array, required)
- `nextCursor` (string | null, required): Pass as cursor to get the next page; null on the last page.

## FAQ

### What does "Audit a Shopify store" do?

Reads the health data of the signed-in Shopify store: its name, domain, plan and currency; how many products it has by status, how many orders in the last 30 days and how many customers; and one page of products, most recently updated first, with whether each has an image, the length of its description, its lowest price and its stock. Use these fields to spot catalogue problems such as missing images, empty descriptions, zero prices or active products out of stock. Pass nextCursor back as cursor for the next page. Read-only.

### What information do I need to provide?

Optional: limit, store, cursor.

### What does it return?

It returns shop, count, store, counts, hasMore, products, nextCursor.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It only reads. It looks things up on admin.shopify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/get_store_audit, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/get_store_audit

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/get_store_audit
