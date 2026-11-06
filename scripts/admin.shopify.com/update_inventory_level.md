# Set a Shopify product's available stock

Automatically set a Shopify product's available stock on admin.shopify.com. Sets the available quantity of one product variant at one location of the signed-in Shopify store, found by its SKU, the way the admin's Stock page does, then reloads the stock list to confirm the new quantity. Returns the quantities before and after, the variant, the SKU and the location. A quantity already at the target is left alone. A rehearsal mode shows the current quantity without changing anything. The variant must have stock tracking on; an unknown SKU, or a SKU shared by several variants, fails with a message that says so. For a store with several locations, pass the location.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/update_inventory_level`
- Updated: 2026-11-05 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/update_inventory_level`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/update_inventory_level
```

## Input

- `sku` (string, required): The variant's SKU, exactly as in the admin (admin.shopify.com/list_products shows a product's variants and their SKUs on the product page).
- `available` (integer, required): The available quantity to set at the location.
- `store` (string, optional): The store handle as it appears in the admin URL. Omit it to use the store the signed-in admin opens by default.
- `dryRun` (boolean, optional): Read the current quantity and report what would change, without changing anything.
- `locationId` (string, optional): Numeric id of the location (from admin.shopify.com/store/<store>/settings/locations/<id>). Omit to use the location the Stock page shows by default; required when the store has several locations.

## Output

- `sku` (string, required)
- `after` (integer | null, required): Available quantity read back after the change (equal to before when nothing changed).
- `store` (string, required)
- `before` (integer | null, required): Available quantity before the run.
- `dryRun` (boolean, required)
- `changed` (boolean, required): True only when the quantity was changed and read back at the target.
- `variantId` (string | null, optional)
- `locationId` (string | null, optional)
- `variantName` (string | null, optional)
- `locationName` (string | null, optional)

## FAQ

### What does "Set a Shopify product's available stock" do?

Sets the available quantity of one product variant at one location of the signed-in Shopify store, found by its SKU, the way the admin's Stock page does, then reloads the stock list to confirm the new quantity. Returns the quantities before and after, the variant, the SKU and the location. A quantity already at the target is left alone. A rehearsal mode shows the current quantity without changing anything. The variant must have stock tracking on; an unknown SKU, or a SKU shared by several variants, fails with a message that says so. For a store with several locations, pass the location.

### How do I automatically set a Shopify product's available stock on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/update_inventory_level, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/update_inventory_level

### Is there a admin.shopify.com API to set a Shopify product's available stock?

You do not need one. "Set a Shopify product's available stock" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Required: sku, available. Optional: store, dryRun, locationId.

### What does it return?

It returns sku, after, store, before, dryRun, changed, variantId, locationId, variantName, locationName.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It makes changes on admin.shopify.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/update_inventory_level, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/update_inventory_level

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/update_inventory_level
