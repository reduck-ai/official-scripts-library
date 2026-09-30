# Audit a Shopify store

Gives a health check of the signed-in Shopify store: its name, domain, plan and currency; how many products it has by status, how many orders in the last 30 days and how many customers; and a list of catalogue problems to fix, such as products with no image, no description, a zero price, or active products that are out of stock. Read-only.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/get_store_audit`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/get_store_audit`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/get_store_audit
```

## Input

- `store` (string, optional): The store handle as it appears in the admin URL. Omit it to use the store the signed-in admin opens by default.
- `maxProducts` (integer, optional): How many products to inspect for catalogue problems (newest first).

## Output

- `shop` (object, required)
- `store` (string, required)
- `counts` (object, required)
- `issues` (object, required): Each list holds {id, title, status, adminUrl} for the affected products.
- `productsInspected` (integer, required)
- `issueCount` (integer, optional)

## FAQ

### What does "Audit a Shopify store" do?

Gives a health check of the signed-in Shopify store: its name, domain, plan and currency; how many products it has by status, how many orders in the last 30 days and how many customers; and a list of catalogue problems to fix, such as products with no image, no description, a zero price, or active products that are out of stock. Read-only.

### What information do I need to provide?

Optional: store, maxProducts.

### What does it return?

It returns shop, store, counts, issues, issueCount, productsInspected.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It only reads. It looks things up on admin.shopify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/get_store_audit, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/get_store_audit

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/get_store_audit
