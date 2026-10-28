# Identify the buyer on the Musée d'Orsay ticket shop

Give the buyer's email to the official Musée d'Orsay ticket shop, for the basket filled with add_to_cart, and report what the shop needs before payment. Every order needs a Musée d'Orsay customer account, and the shop only keeps a new account once its first order is paid. A browser already identified returns already_identified and changes nothing. Otherwise the email decides: an existing account returns sign_in_required (sign in with its password in this browser), an unknown email returns new_customer_details_required with the sign-up fields the shop asks for (name, email, password, country). The script never types a password, never creates an account and stops before payment: run complete_booking next.

- Site: billetterie.musee-orsay.fr
- Address: `reduck/billetterie.musee-orsay.fr/fill_booking_details`
- Updated: 2026-10-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/billetterie.musee-orsay.fr/fill_booking_details`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/fill_booking_details
```

## Input

- `email` (string, optional): The buyer's email. Not needed when the browser is already identified.

## Output

- `status` (string, required)
- `allFilled` (boolean, required)
- `requiredFields` (array, required)

## FAQ

### What does "Identify the buyer on the Musée d'Orsay ticket shop" do?

Give the buyer's email to the official Musée d'Orsay ticket shop, for the basket filled with add_to_cart, and report what the shop needs before payment. Every order needs a Musée d'Orsay customer account, and the shop only keeps a new account once its first order is paid. A browser already identified returns already_identified and changes nothing. Otherwise the email decides: an existing account returns sign_in_required (sign in with its password in this browser), an unknown email returns new_customer_details_required with the sign-up fields the shop asks for (name, email, password, country). The script never types a password, never creates an account and stops before payment: run complete_booking next.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns status, allFilled, requiredFields.

### Do I need to be logged in to billetterie.musee-orsay.fr?

No. It only uses pages of billetterie.musee-orsay.fr that are reachable without signing in.

### Does it change anything on billetterie.musee-orsay.fr, or only read data?

It only reads. It looks things up on billetterie.musee-orsay.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/billetterie.musee-orsay.fr/fill_booking_details, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/fill_booking_details

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/billetterie.musee-orsay.fr/fill_booking_details
