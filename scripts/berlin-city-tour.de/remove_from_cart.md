# Remove a line from the Berlin City Tour basket

Automatically remove a line from the Berlin City Tour basket on berlin-city-tour.de. Takes one line out of a Berlin City Tour basket, using the cartId and cartPackageGroupId that add_to_cart returned, and reports what the basket holds afterwards. This is the counterpart to add_to_cart: because the shop merges repeated adds for one travel date into a single line, a run that was retried leaves more guests on that date than intended, and this is how that is undone. It refuses when the basket has no such line, and it checks the line is really gone before reporting success rather than trusting the request it sent.

- Site: berlin-city-tour.de
- Address: `reduck/berlin-city-tour.de/remove_from_cart`
- Updated: 2026-11-13 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/berlin-city-tour.de/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/remove_from_cart
```

## Input

- `cartId` (string, required): The basket, as add_to_cart returned it.
- `cartPackageGroupId` (string, required): The basket line to remove, as add_to_cart returned it.

## Output

- `cartId` (string, required)
- `cartTotal` (number, required)
- `remainingLines` (array, required)
- `removedGroupId` (string, required)
- `removedQuantity` (integer, required): How many guests the removed line held.
- `currency` (string | null, optional)

## FAQ

### What does "Remove a line from the Berlin City Tour basket" do?

Takes one line out of a Berlin City Tour basket, using the cartId and cartPackageGroupId that add_to_cart returned, and reports what the basket holds afterwards. This is the counterpart to add_to_cart: because the shop merges repeated adds for one travel date into a single line, a run that was retried leaves more guests on that date than intended, and this is how that is undone. It refuses when the basket has no such line, and it checks the line is really gone before reporting success rather than trusting the request it sent.

### How do I automatically remove a line from the Berlin City Tour basket on berlin-city-tour.de?

Ask an AI agent connected to Reduck to run reduck/berlin-city-tour.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/remove_from_cart

### Is there a berlin-city-tour.de API to remove a line from the Berlin City Tour basket?

You do not need one. "Remove a line from the Berlin City Tour basket" drives the real berlin-city-tour.de pages in a browser, so it works whether or not berlin-city-tour.de offers an API for this.

### What information do I need to provide?

Required: cartId, cartPackageGroupId.

### What does it return?

It returns cartId, currency, cartTotal, remainingLines, removedGroupId, removedQuantity.

### Do I need to be logged in to berlin-city-tour.de?

No. It only uses pages of berlin-city-tour.de that are reachable without signing in.

### Does it change anything on berlin-city-tour.de, or only read data?

It makes changes on berlin-city-tour.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/berlin-city-tour.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/remove_from_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/berlin-city-tour.de/remove_from_cart
