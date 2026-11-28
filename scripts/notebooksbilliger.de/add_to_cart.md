# Add to notebooksbilliger.de cart

Automatically add to notebooksbilliger.de cart on notebooksbilliger.de. Add one notebooksbilliger.de product to the cart of this browser, by its link. Returns the cart after the add, with a review_hash per line. The site can add a free add-on with some products (for example an antivirus subscription free for the first year); it appears as its own line. On a browser that does not keep the site's cookies between runs, the cart does not persist.

- Site: notebooksbilliger.de
- Address: `reduck/notebooksbilliger.de/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notebooksbilliger.de/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/add_to_cart
```

## Input

- `url` (string, required): The product's link as Search notebooksbilliger.de products returns it, ending in +<id>.

## Output

- `added` (object, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "Add to notebooksbilliger.de cart" do?

Add one notebooksbilliger.de product to the cart of this browser, by its link. Returns the cart after the add, with a review_hash per line. The site can add a free add-on with some products (for example an antivirus subscription free for the first year); it appears as its own line. On a browser that does not keep the site's cookies between runs, the cart does not persist.

### How do I automatically add to notebooksbilliger.de cart on notebooksbilliger.de?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/add_to_cart

### Is there a notebooksbilliger.de API to add to notebooksbilliger.de cart?

You do not need one. "Add to notebooksbilliger.de cart" drives the real notebooksbilliger.de pages in a browser, so it works whether or not notebooksbilliger.de offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns added, count, lines, total.

### Do I need to be logged in to notebooksbilliger.de?

No. It only uses pages of notebooksbilliger.de that are reachable without signing in.

### Does it change anything on notebooksbilliger.de, or only read data?

It makes changes on notebooksbilliger.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/notebooksbilliger.de/add_to_cart
