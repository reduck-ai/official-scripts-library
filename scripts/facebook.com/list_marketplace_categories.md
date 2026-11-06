# List Facebook Marketplace categories

Automatically list Facebook Marketplace categories on facebook.com. List the top-level Facebook Marketplace categories shown in the search sidebar, with the category id that search_marketplace_listings takes. Special sections without a category id (free items, property rentals) come back with categoryId null and their section. Names follow the account's interface language.

- Site: facebook.com
- Address: `reduck/facebook.com/list_marketplace_categories`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/list_marketplace_categories`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_marketplace_categories
```

## Input

It takes no input.

## Output

- `categories` (array, required)

## FAQ

### What does "List Facebook Marketplace categories" do?

List the top-level Facebook Marketplace categories shown in the search sidebar, with the category id that search_marketplace_listings takes. Special sections without a category id (free items, property rentals) come back with categoryId null and their section. Names follow the account's interface language.

### How do I automatically list Facebook Marketplace categories on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_marketplace_categories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_marketplace_categories

### Is there a facebook.com API to list Facebook Marketplace categories?

You do not need one. "List Facebook Marketplace categories" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns categories.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_marketplace_categories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_marketplace_categories

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/list_marketplace_categories
