# Get a Shopify order

Automatically get a Shopify order on admin.shopify.com. Returns the full details of one order in the signed-in Shopify store, found by its order number, id or admin link: customer, contact details, payment and fulfilment status, subtotal, shipping, tax, discounts and total, shipping and billing addresses, and every line item with its quantity and price.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/get_order`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/get_order`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/get_order
```

## Input

- `order` (string, required): The order number (e.g. #1001 or 1001), its id, or its admin link (from admin.shopify.com/list_orders).
- `store` (string, optional): The store handle as it appears in the admin URL. Omit it to use the store the signed-in admin opens by default.

## Output

- `id` (string, required)
- `name` (string, required)
- `store` (string, required)
- `lineItems` (array, required)
- `gid` (string, optional)
- `tax` (string | null, optional)
- `note` (string | null, optional)
- `tags` (array, optional)
- `test` (boolean, optional)
- `email` (string | null, optional)
- `phone` (string | null, optional)
- `total` (string | null, optional)
- `closed` (boolean, optional)
- `adminUrl` (string, optional)
- `currency` (string | null, optional)
- `customer` (object | null, optional)
- `shipping` (string | null, optional)
- `subtotal` (string | null, optional)
- `cancelled` (boolean, optional)
- `createdAt` (string, optional)
- `discounts` (string | null, optional)
- `outstanding` (string | null, optional)
- `processedAt` (string | null, optional)
- `cancelReason` (string | null, optional)
- `billingAddress` (object | null, optional)
- `financialStatus` (string | null, optional)
- `shippingAddress` (object | null, optional)
- `fulfillmentStatus` (string | null, optional)

## FAQ

### What does "Get a Shopify order" do?

Returns the full details of one order in the signed-in Shopify store, found by its order number, id or admin link: customer, contact details, payment and fulfilment status, subtotal, shipping, tax, discounts and total, shipping and billing addresses, and every line item with its quantity and price.

### How do I automatically get a Shopify order on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/get_order, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/get_order

### Is there a admin.shopify.com API to get a Shopify order?

You do not need one. "Get a Shopify order" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Required: order. Optional: store.

### What does it return?

It returns id, gid, tax, name, note, tags, test, email, phone, store, total, closed, adminUrl, currency, customer, shipping, subtotal, cancelled, createdAt, discounts, lineItems, outstanding, processedAt, cancelReason, billingAddress, financialStatus, shippingAddress, fulfillmentStatus.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It only reads. It looks things up on admin.shopify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/get_order, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/get_order

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/get_order
