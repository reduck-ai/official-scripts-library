# Create a Shopify product

Automatically create a Shopify product on admin.shopify.com. Creates a product in the signed-in Shopify store with a title and, optionally, a description, vendor, type, tags, price, compare-at price and SKU. Products are created as drafts unless another status is asked for. Reports any existing product with the same title and confirms the new product by reading it back. A rehearsal mode shows what would be created without creating anything.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/create_product`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/create_product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/create_product
```

## Input

- `title` (string, required): The product title.
- `sku` (string, optional)
- `tags` (array, optional)
- `price` (number, optional): Price of the product's default variant, in the store currency.
- `store` (string, optional): The store handle as it appears in the admin URL. Omit it to use the store the signed-in admin opens by default.
- `dryRun` (boolean, optional): Check the store and report what would be created, without creating anything.
- `status` (string, optional): Draft keeps the product off the storefront; active publishes it.
- `vendor` (string, optional)
- `description` (string, optional): Plain-text description; blank lines separate paragraphs.
- `productType` (string, optional)
- `compareAtPrice` (number, optional): Original price shown struck through next to the price.

## Output

- `store` (string, required)
- `dryRun` (boolean, required)
- `created` (boolean, required)
- `alreadyExists` (array, required): Products already in the store with the same title.
- `product` (object, optional)
- `wouldCreate` (object, optional)

## FAQ

### What does "Create a Shopify product" do?

Creates a product in the signed-in Shopify store with a title and, optionally, a description, vendor, type, tags, price, compare-at price and SKU. Products are created as drafts unless another status is asked for. Reports any existing product with the same title and confirms the new product by reading it back. A rehearsal mode shows what would be created without creating anything.

### How do I automatically create a Shopify product on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/create_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/create_product

### Is there a admin.shopify.com API to create a Shopify product?

You do not need one. "Create a Shopify product" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Required: title. Optional: sku, tags, price, store, dryRun, status, vendor, description, productType, compareAtPrice.

### What does it return?

It returns store, dryRun, created, product, wouldCreate, alreadyExists.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It makes changes on admin.shopify.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/create_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/create_product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/create_product
