# List Shopify store orders

Automatically list Shopify store orders on admin.shopify.com. Lists orders from the signed-in Shopify admin, with the order number, customer, total, payment and fulfilment status and date.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/list_orders`
- Updated: 2026-09-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/list_orders`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_orders
```

## Input

- `limit` (integer, optional): Maximum number of orders to return.
- `query` (string, optional): Free-text search as typed in the admin's order search box (order number, customer name or email, and more). Shopify search syntax such as tag:wholesale is also accepted.
- `store` (string, optional): The store handle as it appears in the admin URL. Omit it to use the store the signed-in admin opens by default.
- `status` (string, optional): Only return orders with this order status.
- `financialStatus` (string, optional): Only return orders with this payment status.
- `fulfillmentStatus` (string, optional): Only return orders with this fulfilment status.

## Output

- `count` (integer, required)
- `store` (string, required)
- `orders` (array, required)
- `search` (string | null, required): The search string sent to Shopify, or null when unfiltered.
- `hasMore` (boolean, required)
- `shopName` (string | null, optional)

## FAQ

### What does "List Shopify store orders" do?

Lists orders from the signed-in Shopify admin, with the order number, customer, total, payment and fulfilment status and date.

### How do I automatically list Shopify store orders on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/list_orders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_orders

### Is there a admin.shopify.com API to list Shopify store orders?

You do not need one. "List Shopify store orders" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Optional: limit, query, store, status, financialStatus, fulfillmentStatus.

### What does it return?

It returns count, store, orders, search, hasMore, shopName.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It only reads. It looks things up on admin.shopify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/list_orders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_orders

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/list_orders
