# Preview a Facebook Marketplace listing

Fill the Facebook Marketplace "sell an item" form with a photo, title, price, category, condition and description, and return what the form and its preview hold, without publishing or saving a draft. Use it to check a listing before posting it. Category and condition are the labels the form shows in the account's interface language. Leaving the page discards everything; nothing is created on the account.

- Site: facebook.com
- Address: `reduck/facebook.com/preview_marketplace_listing`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/preview_marketplace_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/preview_marketplace_listing
```

## Input

- `photo` (string, required): Photo of the item (jpg or png).
- `price` (integer, required): Price in the account's currency, whole units.
- `title` (string, required)
- `category` (string, required): Category label exactly as the form lists it, e.g. Meubles.
- `condition` (string, optional): Condition label as the form lists it, e.g. Neuf.
- `description` (string, optional)

## Output

- `price` (string | null, required)
- `title` (string | null, required)
- `category` (string | null, required)
- `published` (boolean, required)
- `nextEnabled` (boolean, required): Whether the form would let you go on to the next step.
- `condition` (string | null, optional)
- `photoCount` (integer | null, optional)
- `description` (string | null, optional)

## FAQ

### What does "Preview a Facebook Marketplace listing" do?

Fill the Facebook Marketplace "sell an item" form with a photo, title, price, category, condition and description, and return what the form and its preview hold, without publishing or saving a draft. Use it to check a listing before posting it. Category and condition are the labels the form shows in the account's interface language. Leaving the page discards everything; nothing is created on the account.

### What information do I need to provide?

Required: photo, title, price, category. Optional: condition, description.

### What does it return?

It returns price, title, category, condition, published, photoCount, description, nextEnabled.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/preview_marketplace_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/preview_marketplace_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/preview_marketplace_listing
