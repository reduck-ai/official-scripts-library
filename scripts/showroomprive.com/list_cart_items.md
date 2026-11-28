# List Showroomprivé cart items

Automatically list Showroomprivé cart items on showroomprive.com. List the products in the showroomprive.com basket of the signed-in member.

- Site: showroomprive.com
- Address: `reduck/showroomprive.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/showroomprive.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `item_count` (integer, required)
- `total` (number | null, optional): Basket total before delivery
- `currency` (string, optional)
- `reserved_for_seconds` (integer | null, optional): How long the site still holds the items for the member

## FAQ

### What does "List Showroomprivé cart items" do?

List the products in the showroomprive.com basket of the signed-in member.

### How do I automatically list Showroomprivé cart items on showroomprive.com?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/list_cart_items

### Is there a showroomprive.com API to list Showroomprivé cart items?

You do not need one. "List Showroomprivé cart items" drives the real showroomprive.com pages in a browser, so it works whether or not showroomprive.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, total, currency, item_count, reserved_for_seconds.

### Do I need to be logged in to showroomprive.com?

Yes. It acts as you on showroomprive.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for showroomprive.com.

### Does it change anything on showroomprive.com, or only read data?

It only reads. It looks things up on showroomprive.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/showroomprive.com/list_cart_items
