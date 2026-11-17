# Fill Berlin City Tour booking details

Takes a Berlin City Tour basket made by add_to_cart, enters the traveller's name, email and phone on the checkout, accepts the supplier's terms on the caller's behalf, and stops on the payment page. It pays nothing and never touches a card. It refuses before filling anything when the basket is not the one that was reviewed (review_hash) or does not cost expectedTotal. The shop keeps the traveller on the basket, so pay can continue from there: the result returns what the shop stored. The basket holds its prices for about ten minutes.

- Site: berlin-city-tour.de
- Address: `reduck/berlin-city-tour.de/fill_booking_details`
- Updated: 2026-11-16 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/berlin-city-tour.de/fill_booking_details`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/fill_booking_details
```

## Input

- `cartId` (string, required): The basket, as add_to_cart returned it.
- `acceptTerms` (boolean, required): Must be true: the caller accepts the supplier's terms and conditions and privacy policy for this booking.
- `review_hash` (string, required): The review_hash add_to_cart returned for this basket line. Nothing is filled in when the basket no longer matches it.
- `customerEmail` (string, required): Where the supplier sends the voucher.
- `customerPhone` (string, required): In international form, starting with a plus and the country code, for example +49 30 1234567.
- `expectedTotal` (number, required): The total in euros the customer agreed to. Nothing is filled in when the basket total differs.
- `customerLastName` (string, required)
- `customerFirstName` (string, required)
- `cartPackageGroupId` (string, required): The basket line, as add_to_cart returned it.

## Output

- `stage` (string, required): Always stopped_on_payment_page.
- `cartId` (string, required)
- `guests` (integer, required)
- `currency` (string | null, required)
- `amountDue` (number, required)
- `travelDate` (string | null, required)
- `storedCustomer` (object, required): What the shop now holds on the basket for the traveller.
- `cartPackageGroupId` (string, required)

## FAQ

### What does "Fill Berlin City Tour booking details" do?

Takes a Berlin City Tour basket made by add_to_cart, enters the traveller's name, email and phone on the checkout, accepts the supplier's terms on the caller's behalf, and stops on the payment page. It pays nothing and never touches a card. It refuses before filling anything when the basket is not the one that was reviewed (review_hash) or does not cost expectedTotal. The shop keeps the traveller on the basket, so pay can continue from there: the result returns what the shop stored. The basket holds its prices for about ten minutes.

### What information do I need to provide?

Required: cartId, cartPackageGroupId, review_hash, expectedTotal, customerFirstName, customerLastName, customerEmail, customerPhone, acceptTerms.

### What does it return?

It returns stage, cartId, guests, currency, amountDue, travelDate, storedCustomer, cartPackageGroupId.

### Do I need to be logged in to berlin-city-tour.de?

No. It only uses pages of berlin-city-tour.de that are reachable without signing in.

### Does it change anything on berlin-city-tour.de, or only read data?

It makes changes on berlin-city-tour.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/berlin-city-tour.de/fill_booking_details, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/fill_booking_details

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/berlin-city-tour.de/fill_booking_details
