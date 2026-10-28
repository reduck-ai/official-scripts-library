# Fill Jewish Museum Berlin booking details

Give the booker's details to the official Jewish Museum Berlin ticket shop as a guest, so the basket filled with add_to_cart can be ordered with complete_booking. The guest form asks for first name, last name, email, postcode, country and correspondence language, and the shop's terms and conditions must be accepted (acceptTerms). No password and no customer account are created; the tickets are sent to the email. Returns the fields the shop requires and whether each is filled. A browser already signed in, as a guest or with an account, returns already_identified and changes nothing. It stops before the order: run complete_booking next.

- Site: tickets.jmberlin.de
- Address: `reduck/tickets.jmberlin.de/fill_booking_details`
- Updated: 2026-10-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tickets.jmberlin.de/fill_booking_details`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/fill_booking_details
```

## Input

- `email` (string, required): The address the tickets are sent to.
- `lastName` (string, required)
- `postcode` (string, required)
- `firstName` (string, required)
- `acceptTerms` (boolean, required): Accept the shop's terms and conditions, which it requires for every order.
- `country` (string, optional): Country name as the shop lists it in the chosen language, or its id.
- `language` (string, optional)
- `newsletter` (boolean, optional)
- `correspondenceLanguage` (string, optional): Language of the shop's emails.

## Output

- `status` (string, required)
- `allFilled` (boolean, required)
- `requiredFields` (array, required)
- `guest` (boolean | null, optional)

## FAQ

### What does "Fill Jewish Museum Berlin booking details" do?

Give the booker's details to the official Jewish Museum Berlin ticket shop as a guest, so the basket filled with add_to_cart can be ordered with complete_booking. The guest form asks for first name, last name, email, postcode, country and correspondence language, and the shop's terms and conditions must be accepted (acceptTerms). No password and no customer account are created; the tickets are sent to the email. Returns the fields the shop requires and whether each is filled. A browser already signed in, as a guest or with an account, returns already_identified and changes nothing. It stops before the order: run complete_booking next.

### What information do I need to provide?

Required: firstName, lastName, email, postcode, acceptTerms. Optional: country, language, newsletter, correspondenceLanguage.

### What does it return?

It returns guest, status, allFilled, requiredFields.

### Do I need to be logged in to tickets.jmberlin.de?

No. It only uses pages of tickets.jmberlin.de that are reachable without signing in.

### Does it change anything on tickets.jmberlin.de, or only read data?

It makes changes on tickets.jmberlin.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tickets.jmberlin.de/fill_booking_details, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/fill_booking_details

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tickets.jmberlin.de/fill_booking_details
