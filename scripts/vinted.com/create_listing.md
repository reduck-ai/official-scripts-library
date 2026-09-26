# Create a Vinted listing

Automatically create a Vinted listing on vinted.com. Create a for-sale listing on Vinted from a photo, title, description, category, condition, price and package size (plus an ISBN for books). Works on whichever Vinted country site the browser is signed in to. Defaults to a dry run that fills the whole form and publishes nothing; saveAsDraft keeps the listing private, otherwise it is published. Confirms the result by reopening the saved item. Categories that also ask for brand or size, such as clothing, are refused for now rather than listed incomplete.

- Site: vinted.com
- Address: `reduck/vinted.com/create_listing`
- Updated: 2026-09-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vinted.com/create_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vinted.com/create_listing
```

## Input

- `photo` (string, required): One JPEG/PNG/WebP photo of the item. Vinted requires at least one.
- `price` (number, required): Asking price in the account's currency.
- `title` (string, required)
- `condition` (string, required)
- `description` (string, required)
- `packageSize` (string, required)
- `categoryPath` (array, required): Vinted catalog ids from the top level down to the final category, e.g. [2309, 2312, 2319] for Books & Media > Books > Fiction. Ids are the same in every language.
- `isbn` (string, optional): Optional, book categories only.
- `dryRun` (boolean, optional): When true (the default) the form is filled and checked but nothing is saved or published.
- `saveAsDraft` (boolean, optional): Save the listing as a private draft instead of publishing it.

## Output

- `action` (string, required)
- `dryRun` (boolean, required)
- `domain` (string, optional)
- `itemId` (string | null, optional)
- `itemUrl` (string | null, optional)
- `category` (string | null, optional): The final category's name as Vinted displays it.
- `photosUploaded` (number, optional)

## FAQ

### What does "Create a Vinted listing" do?

Create a for-sale listing on Vinted from a photo, title, description, category, condition, price and package size (plus an ISBN for books). Works on whichever Vinted country site the browser is signed in to. Defaults to a dry run that fills the whole form and publishes nothing; saveAsDraft keeps the listing private, otherwise it is published. Confirms the result by reopening the saved item. Categories that also ask for brand or size, such as clothing, are refused for now rather than listed incomplete.

### How do I automatically create a Vinted listing on vinted.com?

Ask an AI agent connected to Reduck to run reduck/vinted.com/create_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/create_listing

### Is there a vinted.com API to create a Vinted listing?

You do not need one. "Create a Vinted listing" drives the real vinted.com pages in a browser, so it works whether or not vinted.com offers an API for this.

### What information do I need to provide?

Required: photo, title, description, categoryPath, condition, price, packageSize. Optional: isbn, dryRun, saveAsDraft.

### What does it return?

It returns action, domain, dryRun, itemId, itemUrl, category, photosUploaded.

### Do I need to be logged in to vinted.com?

Yes. It acts as you on vinted.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vinted.com cookies saved by the Reduck extension.

### Does it change anything on vinted.com, or only read data?

It makes changes on vinted.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vinted.com/create_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/create_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vinted.com/create_listing
