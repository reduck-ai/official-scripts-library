# Update a Shopify product

Automatically update a Shopify product on admin.shopify.com. Changes an existing product in the signed-in Shopify store, found by its id, admin link or handle: its title, description, vendor, type, status, or tags (replace them all, or add and remove individual tags). Fields already at the requested value are left alone, and the product is read back afterwards to confirm what changed. A rehearsal mode shows the current and new values without changing anything. Use admin.shopify.com/update_product_price for prices.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/update_product`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/update_product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/update_product
```

## Input

- `product` (string, required): The product's id, its admin link, or its handle (from admin.shopify.com/list_products).
- `tags` (array, optional): Replace all tags with exactly these.
- `store` (string, optional): The store handle as it appears in the admin URL. Omit it to use the store the signed-in admin opens by default.
- `title` (string, optional)
- `dryRun` (boolean, optional): Report the current and new values without changing anything.
- `status` (string, optional): Active publishes the product; draft hides it from the storefront.
- `vendor` (string, optional)
- `addTags` (array, optional): Tags to add, keeping the existing ones.
- `removeTags` (array, optional): Tags to remove, keeping the others.
- `description` (string, optional): New plain-text description; blank lines separate paragraphs. An empty string clears it.
- `productType` (string, optional)

## Output

- `store` (string, required)
- `dryRun` (boolean, required)
- `changes` (array, required): One entry per field that differs from the request.
- `product` (object, required)
- `updated` (boolean, required): False when nothing needed changing, or in a rehearsal.

## FAQ

### What does "Update a Shopify product" do?

Changes an existing product in the signed-in Shopify store, found by its id, admin link or handle: its title, description, vendor, type, status, or tags (replace them all, or add and remove individual tags). Fields already at the requested value are left alone, and the product is read back afterwards to confirm what changed. A rehearsal mode shows the current and new values without changing anything. Use admin.shopify.com/update_product_price for prices.

### How do I automatically update a Shopify product on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/update_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/update_product

### Is there a admin.shopify.com API to update a Shopify product?

You do not need one. "Update a Shopify product" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: tags, store, title, dryRun, status, vendor, addTags, removeTags, description, productType.

### What does it return?

It returns store, dryRun, changes, product, updated.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It makes changes on admin.shopify.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/update_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/update_product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/update_product
