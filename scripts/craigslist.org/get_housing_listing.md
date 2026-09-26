# Craigslist API: get a Craigslist apartment listing

Automatically get a Craigslist apartment listing on craigslist.org. An unofficial Craigslist API for one apartment listing: address, rent, photos, amenities and the full description as data, from its link. Read one Craigslist housing listing (an apartment, a room or a sublet) from its link, as returned by search_housing. Returns the post id, title, asking rent, the size line (bedrooms and square feet), neighborhood, street address and ZIP code when the poster gave them, map coordinates, bedrooms, bathrooms, whether pets and smoking are allowed, every amenity the listing shows (rent period, laundry, parking, housing type, cats and dogs, furnished, availability date and others), the full description, all photo links, and when it was posted and last updated. A listing that the poster deleted or Craigslist removed comes back as not found rather than as an error. Phone numbers the poster hid behind the site's contact button are not revealed.

- Site: craigslist.org
- Address: `reduck/craigslist.org/get_housing_listing`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/craigslist.org/get_housing_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/craigslist.org/get_housing_listing
```

## Input

- `url` (string, required): The listing's page, e.g. https://www.craigslist.org/view/d/san-francisco-sunny-1br/1xpNaQ2v8YtyoDNKXYd6SQ, as search_housing returns it. The older https://<city>.craigslist.org/.../<post id>.html form works too.

## Output

- `url` (string, required): The page as the site resolved it.
- `found` (boolean, required): false when the listing no longer exists (deleted, expired or removed); every other field is then absent.
- `body` (string | null, optional): The full description as shown.
- `price` (string | null, optional): Asking rent as shown, e.g. "$2,100".
- `title` (string | null, optional)
- `images` (array, optional)
- `postId` (string | null, optional)
- `address` (object | null, optional)
- `housing` (string | null, optional): The size line under the title, e.g. "1br - 525ft2".
- `bedrooms` (number | null, optional)
- `latitude` (number | null, optional)
- `postedAt` (string | null, optional): ISO 8601 with the poster's UTC offset.
- `bathrooms` (number | null, optional)
- `longitude` (number | null, optional)
- `updatedAt` (string | null, optional): ISO 8601; null when never edited.
- `attributes` (array, optional): Every amenity line, in page order. key is the site's own name for it (laundry, parking, housing_type, pets_cat, pets_dog, is_furnished, rent_period, private_room, private_bath, no_smoking…), null for the headline lines (bedrooms/bathrooms, square feet, availability date).
- `petsAllowed` (boolean | null, optional)
- `neighborhood` (string | null, optional): The poster's own location text.
- `smokingAllowed` (boolean | null, optional)

## FAQ

### What does "Craigslist API: get a Craigslist apartment listing" do?

An unofficial Craigslist API for one apartment listing: address, rent, photos, amenities and the full description as data, from its link. Read one Craigslist housing listing (an apartment, a room or a sublet) from its link, as returned by search_housing. Returns the post id, title, asking rent, the size line (bedrooms and square feet), neighborhood, street address and ZIP code when the poster gave them, map coordinates, bedrooms, bathrooms, whether pets and smoking are allowed, every amenity the listing shows (rent period, laundry, parking, housing type, cats and dogs, furnished, availability date and others), the full description, all photo links, and when it was posted and last updated. A listing that the poster deleted or Craigslist removed comes back as not found rather than as an error. Phone numbers the poster hid behind the site's contact button are not revealed.

### How do I automatically get a Craigslist apartment listing on craigslist.org?

Ask an AI agent connected to Reduck to run reduck/craigslist.org/get_housing_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/craigslist.org/get_housing_listing

### Is there a craigslist.org API to get a Craigslist apartment listing?

You do not need one. "Craigslist API: get a Craigslist apartment listing" drives the real craigslist.org pages in a browser, so it works whether or not craigslist.org offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, body, found, price, title, images, postId, address, housing, bedrooms, latitude, postedAt, bathrooms, longitude, updatedAt, attributes, petsAllowed, neighborhood, smokingAllowed.

### Do I need to be logged in to craigslist.org?

No. It only uses pages of craigslist.org that are reachable without signing in.

### Does it change anything on craigslist.org, or only read data?

It only reads. It looks things up on craigslist.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/craigslist.org/get_housing_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/craigslist.org/get_housing_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/craigslist.org/get_housing_listing
