# Get Trustpilot categories

Automatically get Trustpilot categories on trustpilot.com. List Trustpilot's full category tree from the /categories index: each top-level category with its categoryId, displayName and subCategories (the categoryId is the key get_category takes).

- Site: trustpilot.com
- Address: `reduck/trustpilot.com/get_categories`
- Updated: 2026-08-14 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trustpilot.com/get_categories`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_categories
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `categories` (array, required)

## FAQ

### What does "Get Trustpilot categories" do?

List Trustpilot's full category tree from the /categories index: each top-level category with its categoryId, displayName and subCategories (the categoryId is the key get_category takes).

### How do I automatically get Trustpilot categories on trustpilot.com?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_categories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_categories

### Is there a trustpilot.com API to get Trustpilot categories?

You do not need one. "Get Trustpilot categories" drives the real trustpilot.com pages in a browser, so it works whether or not trustpilot.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, categories.

### Do I need to be logged in to trustpilot.com?

No. It only uses pages of trustpilot.com that are reachable without signing in.

### Does it change anything on trustpilot.com, or only read data?

Unknown: its author has not declared whether it changes anything on trustpilot.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_categories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_categories

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trustpilot.com/get_categories
