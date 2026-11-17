# Cancel Amazon.de order

Automatically cancel Amazon.de order on amazon.de. Cancel an Amazon.de order that has not shipped yet, by order number, and confirm the cancellation on the order page. Every item of the order is cancelled; returns the item titles and the order's status afterwards. Orders that already shipped cannot be cancelled this way and fail.

- Site: amazon.de
- Address: `reduck/amazon.de/cancel_order`
- Updated: 2026-11-16 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.de/cancel_order`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.de/cancel_order
```

## Input

- `order_id` (string, required): Amazon order number, e.g. 113-1814615-7224222 (as shown in Your Orders).

## Output

- `items` (array, required): Titles of the items the cancellation was requested for.
- `pending` (boolean, required): True when Amazon accepted the request but is still processing it; the order can still ship. Check the order again later.
- `order_id` (string, required)
- `cancelled` (boolean, required): True when the order page shows the cancellation as done: nothing left to cancel and no request still processing.
- `status` (string | null, optional): Shipment status headline on the order page after the request, as displayed (e.g. Cancelled).

## FAQ

### What does "Cancel Amazon.de order" do?

Cancel an Amazon.de order that has not shipped yet, by order number, and confirm the cancellation on the order page. Every item of the order is cancelled; returns the item titles and the order's status afterwards. Orders that already shipped cannot be cancelled this way and fail.

### How do I automatically cancel Amazon.de order on amazon.de?

Ask an AI agent connected to Reduck to run reduck/amazon.de/cancel_order, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/cancel_order

### Is there a amazon.de API to cancel Amazon.de order?

You do not need one. "Cancel Amazon.de order" drives the real amazon.de pages in a browser, so it works whether or not amazon.de offers an API for this.

### What information do I need to provide?

Required: order_id.

### What does it return?

It returns items, status, pending, order_id, cancelled.

### Do I need to be logged in to amazon.de?

Yes. It acts as you on amazon.de: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.de cookies saved by the Reduck extension.

### Does it change anything on amazon.de, or only read data?

It makes changes on amazon.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.de/cancel_order, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/cancel_order

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.de/cancel_order
