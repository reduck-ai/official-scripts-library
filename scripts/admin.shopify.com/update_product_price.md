# Update a Shopify product's price

Automatically update a Shopify product's price on admin.shopify.com. Changes the price and/or compare-at price of a product in the signed-in Shopify store, found by its id, admin link or handle, then reads the product back to confirm the new prices. For a product with several variants, pick one variant or apply the change to all of them. Prices already at the target are left alone. A rehearsal mode shows the current and new prices without changing anything.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/update_product_price`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/update_product_price`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/update_product_price
```

## Input

- `product` (string, required): The product's id, its admin link, or its handle (from admin.shopify.com/list_products).
- `price` (number, optional): New price, in the store currency.
- `store` (string, optional): The store handle as it appears in the admin URL. Omit it to use the store the signed-in admin opens by default.
- `dryRun` (boolean, optional): Report the current and new prices without changing anything.
- `variantId` (string, optional): Change only this variant. Required when the product has several variants, unless allVariants is set.
- `allVariants` (boolean, optional): Apply the change to every variant of the product.
- `compareAtPrice` (number | null, optional): New compare-at (struck-through) price; null clears it.

## Output

- `store` (string, required)
- `dryRun` (boolean, required)
- `changes` (array, required)
- `product` (object, required)
- `updated` (boolean, required)
- `alreadyAtTarget` (boolean, required): True when every targeted variant already had the requested prices.

## FAQ

### What does "Update a Shopify product's price" do?

Changes the price and/or compare-at price of a product in the signed-in Shopify store, found by its id, admin link or handle, then reads the product back to confirm the new prices. For a product with several variants, pick one variant or apply the change to all of them. Prices already at the target are left alone. A rehearsal mode shows the current and new prices without changing anything.

### How do I automatically update a Shopify product's price on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/update_product_price, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/update_product_price

### Is there a admin.shopify.com API to update a Shopify product's price?

You do not need one. "Update a Shopify product's price" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: price, store, dryRun, variantId, allVariants, compareAtPrice.

### What does it return?

It returns store, dryRun, changes, product, updated, alreadyAtTarget.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It makes changes on admin.shopify.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/update_product_price, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/update_product_price

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/update_product_price
