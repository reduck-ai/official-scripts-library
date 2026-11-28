# Add a product to the Nocibé cart

Automatically add a product to the Nocibé cart on nocibe.fr. Add one size of a Nocibé (nocibe.fr) product, from Nocibé or a partner seller, to the cart of this browser, with a quantity from 1 to 10, as the product page's add to cart button does. Give the product id or link and, for a product with several sizes, the offer_id of one size (from Get Nocibé product); a link with ?variant= names the size itself. Returns the product id, offer id, name, size, seller, the units added and now in the cart, the line's item_id and review_hash (for Remove a product from the Nocibé cart), and the cart's count and subtotal in euros. Works as a guest, with no account: lines already in the cart stay. An unknown product, a size the product does not have, a missing offer_id for a product with several sizes, and a size that is out of stock are refused with an error, and nothing is added. Nothing is paid or ordered. Works in your own browser (the extension); Nocibé refuses cloud browsers.

- Site: nocibe.fr
- Address: `reduck/nocibe.fr/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nocibe.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/add_to_cart
```

## Input

- `product` (string, required): The product id (product_id from Search Nocibé products or Get Nocibé product) or a nocibe.fr product link.
- `offer_id` (string, optional): Code of the size to add (offer_id of a variant from Get Nocibé product). Leave it out for a product with a single size, or when the link names the size (?variant=).
- `quantity` (integer, optional)

## Output

- `added` (integer, required)
- `offer_id` (string, required)
- `product_id` (string, required)
- `name` (string | null, optional)
- `size` (string | null, optional)
- `seller` (string | null, optional)
- `item_id` (string, optional)
- `currency` (string, optional)
- `cart_count` (integer, optional)
- `unit_price` (number | null, optional)
- `review_hash` (string, optional)
- `cart_subtotal` (number, optional)
- `quantity_in_cart` (integer, optional)

## FAQ

### What does "Add a product to the Nocibé cart" do?

Add one size of a Nocibé (nocibe.fr) product, from Nocibé or a partner seller, to the cart of this browser, with a quantity from 1 to 10, as the product page's add to cart button does. Give the product id or link and, for a product with several sizes, the offer_id of one size (from Get Nocibé product); a link with ?variant= names the size itself. Returns the product id, offer id, name, size, seller, the units added and now in the cart, the line's item_id and review_hash (for Remove a product from the Nocibé cart), and the cart's count and subtotal in euros. Works as a guest, with no account: lines already in the cart stay. An unknown product, a size the product does not have, a missing offer_id for a product with several sizes, and a size that is out of stock are refused with an error, and nothing is added. Nothing is paid or ordered. Works in your own browser (the extension); Nocibé refuses cloud browsers.

### How do I automatically add a product to the Nocibé cart on nocibe.fr?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/add_to_cart

### Is there a nocibe.fr API to add a product to the Nocibé cart?

You do not need one. "Add a product to the Nocibé cart" drives the real nocibe.fr pages in a browser, so it works whether or not nocibe.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: offer_id, quantity.

### What does it return?

It returns name, size, added, seller, item_id, currency, offer_id, cart_count, product_id, unit_price, review_hash, cart_subtotal, quantity_in_cart.

### Do I need to be logged in to nocibe.fr?

No. It only uses pages of nocibe.fr that are reachable without signing in.

### Does it change anything on nocibe.fr, or only read data?

It makes changes on nocibe.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nocibe.fr/add_to_cart
