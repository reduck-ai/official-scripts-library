# Add Amazon.fr product to cart

Automatically add Amazon.fr product to cart on amazon.fr. Add a product to your Amazon.fr shopping cart by ASIN, with an optional quantity. Returns the product's cart line after the add (quantity, price) and the cart's item count and subtotal. Products whose page offers only Buy Now or Pre-order now have no add-to-cart button and fail; use Buy Amazon product now for those.

- Site: amazon.fr
- Address: `reduck/amazon.fr/add_to_cart`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/add_to_cart
```

## Input

- `asin` (string, required): Product ASIN, e.g. B000Q5ZDLA.
- `quantity` (integer, optional): How many to add. Must be offered in the product page quantity picker.

## Output

- `asin` (string, required)
- `line` (object | null, required): The product's cart line after the add; null if it is not in the cart.
- `subtotal` (string | null, optional)
- `cart_count` (integer | null, optional)

## FAQ

### What does "Add Amazon.fr product to cart" do?

Add a product to your Amazon.fr shopping cart by ASIN, with an optional quantity. Returns the product's cart line after the add (quantity, price) and the cart's item count and subtotal. Products whose page offers only Buy Now or Pre-order now have no add-to-cart button and fail; use Buy Amazon product now for those.

### How do I automatically add Amazon.fr product to cart on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/add_to_cart

### Is there a amazon.fr API to add Amazon.fr product to cart?

You do not need one. "Add Amazon.fr product to cart" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Required: asin. Optional: quantity.

### What does it return?

It returns asin, line, subtotal, cart_count.

### Do I need to be logged in to amazon.fr?

Yes. It acts as you on amazon.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.fr cookies saved by the Reduck extension.

### Does it change anything on amazon.fr, or only read data?

It makes changes on amazon.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/add_to_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/add_to_cart
