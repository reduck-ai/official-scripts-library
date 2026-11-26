# Remove Amazon.co.uk product from cart

Automatically remove Amazon.co.uk product from cart on amazon.co.uk. Remove a product from your Amazon.co.uk shopping cart by ASIN, whatever its quantity, and return what is left in the cart. A product that is not in the cart is reported as not present rather than failing.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/remove_from_cart
```

## Input

- `asin` (string, required): ASIN of the cart line to delete.

## Output

- `asin` (string, required)
- `remaining` (array, required)
- `was_present` (boolean, required)
- `removed_quantity` (integer | null, optional)

## FAQ

### What does "Remove Amazon.co.uk product from cart" do?

Remove a product from your Amazon.co.uk shopping cart by ASIN, whatever its quantity, and return what is left in the cart. A product that is not in the cart is reported as not present rather than failing.

### How do I automatically remove Amazon.co.uk product from cart on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/remove_from_cart

### Is there a amazon.co.uk API to remove Amazon.co.uk product from cart?

You do not need one. "Remove Amazon.co.uk product from cart" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Required: asin.

### What does it return?

It returns asin, remaining, was_present, removed_quantity.

### Do I need to be logged in to amazon.co.uk?

Yes. It acts as you on amazon.co.uk: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.co.uk.

### Does it change anything on amazon.co.uk, or only read data?

It makes changes on amazon.co.uk, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/remove_from_cart
