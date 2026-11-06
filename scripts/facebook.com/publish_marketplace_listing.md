# Publish a Facebook Marketplace listing

Create a listing on Facebook Marketplace as the signed-in account: photos, title, price, category, condition, description and place. With publish false (the default) the whole form is filled and checked up to the final "publish elsewhere" step and nothing is posted; with publish true the listing goes live on Marketplace only, not in any group. Category is given as the menu labels to click in order, and condition and place as the labels the form shows. Confirm the result with list_my_marketplace_listings.

- Site: facebook.com
- Address: `reduck/facebook.com/publish_marketplace_listing`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/publish_marketplace_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/publish_marketplace_listing
```

## Input

- `price` (integer, required): Price in the account's currency, whole units.
- `title` (string, required)
- `photo1` (string, required): First photo (jpg or png).
- `condition` (string, required): Condition label as the form lists it, e.g. Neuf or D’occasion - bon état.
- `categoryPath` (array, required): Menu labels to click in order, e.g. ["Famille", "Puériculture et enfants"] or ["Pour la maison"].
- `locationQuery` (string, required): Place to type in the form, e.g. Paris 14; the first suggestion is chosen and returned.
- `photo2` (string, optional)
- `photo3` (string, optional)
- `photo4` (string, optional)
- `photo5` (string, optional)
- `photo6` (string, optional)
- `photo7` (string, optional)
- `photo8` (string, optional)
- `publish` (boolean, optional): false stops before the final publish step.
- `description` (string, optional)

## Output

- `price` (string | null, required)
- `title` (string | null, required)
- `category` (string | null, required)
- `finalUrl` (string, required)
- `location` (string | null, required)
- `condition` (string | null, required)
- `listingId` (string | null, required): Id of the new listing when it could be read back from your listings, null otherwise.
- `published` (boolean, required)
- `photoCount` (integer | null, required)
- `publishedToGroups` (integer, required): Always 0: only Marketplace is used.

## FAQ

### What does "Publish a Facebook Marketplace listing" do?

Create a listing on Facebook Marketplace as the signed-in account: photos, title, price, category, condition, description and place. With publish false (the default) the whole form is filled and checked up to the final "publish elsewhere" step and nothing is posted; with publish true the listing goes live on Marketplace only, not in any group. Category is given as the menu labels to click in order, and condition and place as the labels the form shows. Confirm the result with list_my_marketplace_listings.

### What information do I need to provide?

Required: photo1, title, price, categoryPath, condition, locationQuery. Optional: photo2, photo3, photo4, photo5, photo6, photo7, photo8, publish, description.

### What does it return?

It returns price, title, category, finalUrl, location, condition, listingId, published, photoCount, publishedToGroups.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/publish_marketplace_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/publish_marketplace_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/publish_marketplace_listing
