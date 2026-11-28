# Add Amazon.in product to cart

Automatically add Amazon.in product to cart on amazon.in. Add a product to your Amazon.in shopping cart by ASIN, with an optional quantity. Returns the product's cart line after the add (quantity, price) and the cart's item count and subtotal. Products whose page offers only Buy Now or Pre-order now have no add-to-cart button and fail.

- Site: amazon.in
- Address: `reduck/amazon.in/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.in/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.in/add_to_cart
```

## Input

- `asin` (string, required): Product ASIN, e.g. B0D8443PTW.
- `quantity` (integer, optional): How many to add. Must be offered in the product page quantity picker.

## Output

- `asin` (string, required)
- `line` (object | null, required): The product's cart line after the add; null if it is not in the cart.
- `subtotal` (string | null, optional)
- `cart_count` (integer | null, optional)

## FAQ

### What does "Add Amazon.in product to cart" do?

Add a product to your Amazon.in shopping cart by ASIN, with an optional quantity. Returns the product's cart line after the add (quantity, price) and the cart's item count and subtotal. Products whose page offers only Buy Now or Pre-order now have no add-to-cart button and fail.

### How do I automatically add Amazon.in product to cart on amazon.in?

Ask an AI agent connected to Reduck to run reduck/amazon.in/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.in/add_to_cart

### Is there a amazon.in API to add Amazon.in product to cart?

You do not need one. "Add Amazon.in product to cart" drives the real amazon.in pages in a browser, so it works whether or not amazon.in offers an API for this.

### What information do I need to provide?

Required: asin. Optional: quantity.

### What does it return?

It returns asin, line, subtotal, cart_count.

### Do I need to be logged in to amazon.in?

Yes. It acts as you on amazon.in: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.in.

### Does it change anything on amazon.in, or only read data?

It makes changes on amazon.in, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.in/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.in/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.in/add_to_cart
