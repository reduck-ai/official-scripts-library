# List King Jouet products of a category page

Automatically list King Jouet products of a category page on king-jouet.com. List the products of one King Jouet category, brand or franchise page, in the order the site shows them: reference, name, product link, price, original price when on sale, rating, brand, franchise, whether it can be bought on the web site, whether it is under embargo, the labels the card shows (such as pre-order or new product), and the codes of the stores that hold it. Pass the link of the listing page as you see it on the site (for example the Pokemon trading cards page); pass page for the next pages. Returns the number of matching products and pages the site reports, and an empty list when the page shows no product. Use it on a schedule to spot new products and restocks, then add one with King Jouet add to cart.

- Site: king-jouet.com
- Address: `reduck/king-jouet.com/list_products`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/king-jouet.com/list_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/list_products
```

## Input

- `url` (string, required): Link of a King Jouet listing page, such as https://www.king-jouet.com/jeux-jouets/jeux-societes/cartes-a-collectionner/pokemon/page1.htm.
- `page` (integer, optional): Page of the listing to read, starting at 1. The page number in the link is replaced by this one.

## Output

- `page` (integer, required)
- `products` (array, required)
- `total_pages` (integer | null, required)
- `total_products` (integer | null, required): Number of products the site reports for the whole listing.

## FAQ

### What does "List King Jouet products of a category page" do?

List the products of one King Jouet category, brand or franchise page, in the order the site shows them: reference, name, product link, price, original price when on sale, rating, brand, franchise, whether it can be bought on the web site, whether it is under embargo, the labels the card shows (such as pre-order or new product), and the codes of the stores that hold it. Pass the link of the listing page as you see it on the site (for example the Pokemon trading cards page); pass page for the next pages. Returns the number of matching products and pages the site reports, and an empty list when the page shows no product. Use it on a schedule to spot new products and restocks, then add one with King Jouet add to cart.

### How do I automatically list King Jouet products of a category page on king-jouet.com?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/list_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/list_products

### Is there a king-jouet.com API to list King Jouet products of a category page?

You do not need one. "List King Jouet products of a category page" drives the real king-jouet.com pages in a browser, so it works whether or not king-jouet.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: page.

### What does it return?

It returns page, products, total_pages, total_products.

### Do I need to be logged in to king-jouet.com?

No. It only uses pages of king-jouet.com that are reachable without signing in.

### Does it change anything on king-jouet.com, or only read data?

It only reads. It looks things up on king-jouet.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/list_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/list_products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/king-jouet.com/list_products
