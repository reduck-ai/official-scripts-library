# List Amazon.com.au orders

Automatically list Amazon.com.au orders on amazon.com.au. List the orders of your Amazon.com.au account for a period, 10 per page: each order's number, date, total, its items (ASIN and title) and its status as Your Orders shows it, for example "Cancelled" or "Arriving Friday", with the line under it. A period with no orders returns an empty list.

- Site: amazon.com.au
- Address: `reduck/amazon.com.au/list_orders`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.au/list_orders`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/list_orders
```

## Input

- `page` (integer, optional): Page of 10 orders, from 1.
- `time_filter` (string, optional): The period of Your Orders: last30, months-3, or year-YYYY (for example year-2026).

## Output

- `orders` (array, required)
- `has_next_page` (boolean, required)
- `page` (integer, optional)
- `time_filter` (string, optional)

## FAQ

### What does "List Amazon.com.au orders" do?

List the orders of your Amazon.com.au account for a period, 10 per page: each order's number, date, total, its items (ASIN and title) and its status as Your Orders shows it, for example "Cancelled" or "Arriving Friday", with the line under it. A period with no orders returns an empty list.

### How do I automatically list Amazon.com.au orders on amazon.com.au?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/list_orders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/list_orders

### Is there a amazon.com.au API to list Amazon.com.au orders?

You do not need one. "List Amazon.com.au orders" drives the real amazon.com.au pages in a browser, so it works whether or not amazon.com.au offers an API for this.

### What information do I need to provide?

Optional: page, time_filter.

### What does it return?

It returns page, orders, time_filter, has_next_page.

### Do I need to be logged in to amazon.com.au?

Yes. It acts as you on amazon.com.au: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.com.au.

### Does it change anything on amazon.com.au, or only read data?

It only reads. It looks things up on amazon.com.au and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/list_orders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/list_orders

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.au/list_orders
