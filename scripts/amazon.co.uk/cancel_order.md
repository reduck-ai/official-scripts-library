# Cancel Amazon.co.uk order

Automatically cancel Amazon.co.uk order on amazon.co.uk. Cancel an Amazon.co.uk order that has not shipped yet, by order number, and confirm the cancellation on the order page. Every item of the order is cancelled; returns the item titles and the order's status afterwards. Orders that already shipped cannot be cancelled this way and fail.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/cancel_order`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/cancel_order`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/cancel_order
```

## Input

- `order_id` (string, required): Amazon order number, e.g. 202-1814615-7224222 (as shown in Your Orders).

## Output

- `items` (array, required): Titles of the items the cancellation was requested for.
- `pending` (boolean, required): True when Amazon accepted the request but is still processing it; the order can still ship. Check the order again later.
- `order_id` (string, required)
- `cancelled` (boolean, required): True when the order page shows the cancellation as done.
- `status` (string | null, optional): Shipment status headline on the order page after the request, as displayed.

## FAQ

### What does "Cancel Amazon.co.uk order" do?

Cancel an Amazon.co.uk order that has not shipped yet, by order number, and confirm the cancellation on the order page. Every item of the order is cancelled; returns the item titles and the order's status afterwards. Orders that already shipped cannot be cancelled this way and fail.

### How do I automatically cancel Amazon.co.uk order on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/cancel_order, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/cancel_order

### Is there a amazon.co.uk API to cancel Amazon.co.uk order?

You do not need one. "Cancel Amazon.co.uk order" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Required: order_id.

### What does it return?

It returns items, status, pending, order_id, cancelled.

### Do I need to be logged in to amazon.co.uk?

Yes. It acts as you on amazon.co.uk: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.co.uk.

### Does it change anything on amazon.co.uk, or only read data?

It makes changes on amazon.co.uk, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/cancel_order, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/cancel_order

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/cancel_order
