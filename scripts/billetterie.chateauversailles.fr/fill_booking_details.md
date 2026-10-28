# Fill Château de Versailles booking details

Give the visitor details for the cart already filled with add_to_cart on the official Château de Versailles ticket shop, as a guest (no account is created). The shop checks every email address with a 6-digit code it sends to that address, so this runs in two passes on the same browser: first with the email only, which makes the shop send the code and returns status email_code_sent; then again with the same email, the code from that email and the visitor's first and last name, which fills the guest form and returns status details_filled. Returns the fields the shop requires and whether each one is filled. It stops before payment: run complete_booking next. A wrong or expired code fails with an error that says to run the first pass again. An empty cart fails with an error that says to run add_to_cart first.

- Site: billetterie.chateauversailles.fr
- Address: `reduck/billetterie.chateauversailles.fr/fill_booking_details`
- Updated: 2026-10-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/billetterie.chateauversailles.fr/fill_booking_details`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/fill_booking_details
```

## Input

- `email` (string, optional): The email address the tickets go to. The shop sends a 6-digit code to it. Not needed when the browser is already signed in to the shop.
- `phone` (string, optional): Phone number. The guest form does not ask for one; it is filled only if the shop shows a phone field.
- `language` (string, optional)
- `lastName` (string, optional): Last name of the person who books. Needed on the second pass.
- `emailCode` (string, optional): The 6-digit code from the shop's email. Leave it out on the first pass.
- `firstName` (string, optional): First name of the person who books. Needed on the second pass.

## Output

- `status` (string, required)
- `allFilled` (boolean, required)
- `requiredFields` (array, required)
- `email` (string | null, optional)
- `message` (string | null, optional)
- `cartTotal` (number | null, optional)

## FAQ

### What does "Fill Château de Versailles booking details" do?

Give the visitor details for the cart already filled with add_to_cart on the official Château de Versailles ticket shop, as a guest (no account is created). The shop checks every email address with a 6-digit code it sends to that address, so this runs in two passes on the same browser: first with the email only, which makes the shop send the code and returns status email_code_sent; then again with the same email, the code from that email and the visitor's first and last name, which fills the guest form and returns status details_filled. Returns the fields the shop requires and whether each one is filled. It stops before payment: run complete_booking next. A wrong or expired code fails with an error that says to run the first pass again. An empty cart fails with an error that says to run add_to_cart first.

### What information do I need to provide?

Optional: email, phone, language, lastName, emailCode, firstName.

### What does it return?

It returns email, status, message, allFilled, cartTotal, requiredFields.

### Do I need to be logged in to billetterie.chateauversailles.fr?

No. It only uses pages of billetterie.chateauversailles.fr that are reachable without signing in.

### Does it change anything on billetterie.chateauversailles.fr, or only read data?

It makes changes on billetterie.chateauversailles.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/billetterie.chateauversailles.fr/fill_booking_details, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/fill_booking_details

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/billetterie.chateauversailles.fr/fill_booking_details
