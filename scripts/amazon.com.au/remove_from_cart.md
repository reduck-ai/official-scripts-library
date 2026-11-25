# Remove Amazon.com.au product from cart

Automatically remove Amazon.com.au product from cart on amazon.com.au. Remove a product from your Amazon.com.au shopping cart by ASIN, whatever its quantity, and return what is left in the cart. A product that is not in the cart is reported as not present rather than failing.

- Site: amazon.com.au
- Address: `reduck/amazon.com.au/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.au/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/remove_from_cart
```

## Input

- `asin` (string, required): ASIN of the cart line to delete.

## Output

- `asin` (string, required)
- `remaining` (array, required)
- `was_present` (boolean, required)
- `removed_quantity` (integer | null, optional)

## FAQ

### What does "Remove Amazon.com.au product from cart" do?

Remove a product from your Amazon.com.au shopping cart by ASIN, whatever its quantity, and return what is left in the cart. A product that is not in the cart is reported as not present rather than failing.

### How do I automatically remove Amazon.com.au product from cart on amazon.com.au?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/remove_from_cart

### Is there a amazon.com.au API to remove Amazon.com.au product from cart?

You do not need one. "Remove Amazon.com.au product from cart" drives the real amazon.com.au pages in a browser, so it works whether or not amazon.com.au offers an API for this.

### What information do I need to provide?

Required: asin.

### What does it return?

It returns asin, remaining, was_present, removed_quantity.

### Do I need to be logged in to amazon.com.au?

Yes. It acts as you on amazon.com.au: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.com.au.

### Does it change anything on amazon.com.au, or only read data?

It makes changes on amazon.com.au, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.au/remove_from_cart
