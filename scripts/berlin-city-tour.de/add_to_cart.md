# Add a Berlin City Tour ticket to the basket for a date

Automatically add a Berlin City Tour ticket to the basket for a date on berlin-city-tour.de. Puts tickets for one travel date into the Berlin City Tour basket and returns the basket contents it created. Takes the guest counts per price category, as check_availability reports them, and the offer_hash from that same check. Before it writes anything it re-reads what the shop sells on that date and recomputes the hash: if the date, the timeslots or the prices have moved since the check, it adds nothing and refuses with what the shop shows now, so the caller can confirm the new offer and retry. It also refuses a date the shop does not sell, a guest category the product does not offer, and a request for more guests than the remaining capacity. The basket lives in the browser, so the cartPackageGroupId it returns is what the later booking steps work from.

- Site: berlin-city-tour.de
- Address: `reduck/berlin-city-tour.de/add_to_cart`
- Updated: 2026-11-13 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/berlin-city-tour.de/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/add_to_cart
```

## Input

- `date` (string, required): The travel date, as YYYY-MM-DD.
- `guests` (array, required): How many guests in each price category, using the category names check_availability returns.
- `offer_hash` (string, required): The offer_hash from check_availability for the same date and product.
- `packageGroupId` (integer, optional): The product to book. 1137 is the Hop-on Hop-off Classic tour 24h.

## Output

- `date` (string, required)
- `lines` (array, required)
- `cartId` (string, required)
- `currency` (string | null, required)
- `cartTotal` (number, required)
- `lineTotal` (number, required): What the basket line for this date now costs in total, including anything added for it earlier.
- `review_hash` (string, required): Identifies this basket line (product, date, guests, prices, total). Pass it to the step that pays, which refuses if the basket no longer matches.
- `lineQuantity` (integer, required): How many guests the basket line for this date now holds in total.
- `packageGroupId` (integer, required)
- `cartPackageGroupId` (string, required)

## FAQ

### What does "Add a Berlin City Tour ticket to the basket for a date" do?

Puts tickets for one travel date into the Berlin City Tour basket and returns the basket contents it created. Takes the guest counts per price category, as check_availability reports them, and the offer_hash from that same check. Before it writes anything it re-reads what the shop sells on that date and recomputes the hash: if the date, the timeslots or the prices have moved since the check, it adds nothing and refuses with what the shop shows now, so the caller can confirm the new offer and retry. It also refuses a date the shop does not sell, a guest category the product does not offer, and a request for more guests than the remaining capacity. The basket lives in the browser, so the cartPackageGroupId it returns is what the later booking steps work from.

### How do I automatically add a Berlin City Tour ticket to the basket for a date on berlin-city-tour.de?

Ask an AI agent connected to Reduck to run reduck/berlin-city-tour.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/add_to_cart

### Is there a berlin-city-tour.de API to add a Berlin City Tour ticket to the basket for a date?

You do not need one. "Add a Berlin City Tour ticket to the basket for a date" drives the real berlin-city-tour.de pages in a browser, so it works whether or not berlin-city-tour.de offers an API for this.

### What information do I need to provide?

Required: date, guests, offer_hash. Optional: packageGroupId.

### What does it return?

It returns date, lines, cartId, currency, cartTotal, lineTotal, review_hash, lineQuantity, packageGroupId, cartPackageGroupId.

### Do I need to be logged in to berlin-city-tour.de?

No. It only uses pages of berlin-city-tour.de that are reachable without signing in.

### Does it change anything on berlin-city-tour.de, or only read data?

It makes changes on berlin-city-tour.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/berlin-city-tour.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/add_to_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/berlin-city-tour.de/add_to_cart
