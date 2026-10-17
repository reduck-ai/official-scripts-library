# Prepare an Airbnb booking

Open Airbnb's confirm-and-pay page for a listing, dates and guests, signed in, and return what booking it would commit you to, without booking: the price lines and total, what is due today, the payment plans (pay in full, or part now and the rest on a date), the payment method Airbnb would charge, the cancellation policy, and whether the host requires a message. It books nothing and charges nothing. When the listing cannot be booked for those dates it fails with Airbnb's reason; Get Airbnb listing shows the free dates.

- Site: airbnb.com
- Address: `reduck/airbnb.com/prepare_booking`
- Updated: 2026-10-16 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/prepare_booking`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/prepare_booking
```

## Input

- `id` (string, required): Airbnb room id (search_listings returns it).
- `checkin` (string, required)
- `checkout` (string, required)
- `pets` (integer, optional)
- `adults` (integer, optional)
- `infants` (integer, optional)
- `children` (integer, optional)
- `currency` (string, optional)

## Output

- `id` (string, required)
- `checkin` (string, required)
- `checkout` (string, required)
- `available` (boolean, required): False when Airbnb will not book these dates and guests; then only unavailableReason is filled and no confirm page is opened.
- `priceItems` (array, required)
- `paymentPlans` (array, required)
- `total` (object | null, optional)
- `guests` (object, optional)
- `dueToday` (string | null, optional): What the selected payment plan charges when you confirm.
- `checkoutUrl` (string | null, optional): The confirm-and-pay page Airbnb opened for this booking.
- `hostMessage` (string | null, optional): The host's own note shown above the message box.
- `paymentMethod` (object | null, optional)
- `messageRequired` (boolean, optional): True when Airbnb will not confirm without a message to the host.
- `unavailableReason` (string | null, optional): Airbnb's code, e.g. DATE. Null when Airbnb gives none.
- `cancellationPolicy` (string | null, optional): Airbnb's policy code, e.g. CANCEL_FLEXIBLE. Get Airbnb listing with these dates gives its refund milestones.

## FAQ

### What does "Prepare an Airbnb booking" do?

Open Airbnb's confirm-and-pay page for a listing, dates and guests, signed in, and return what booking it would commit you to, without booking: the price lines and total, what is due today, the payment plans (pay in full, or part now and the rest on a date), the payment method Airbnb would charge, the cancellation policy, and whether the host requires a message. It books nothing and charges nothing. When the listing cannot be booked for those dates it fails with Airbnb's reason; Get Airbnb listing shows the free dates.

### What information do I need to provide?

Required: id, checkin, checkout. Optional: pets, adults, infants, children, currency.

### What does it return?

It returns id, total, guests, checkin, checkout, dueToday, available, priceItems, checkoutUrl, hostMessage, paymentPlans, paymentMethod, messageRequired, unavailableReason, cancellationPolicy.

### Do I need to be logged in to airbnb.com?

Yes. It acts as you on airbnb.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the airbnb.com cookies saved by the Reduck extension.

### Does it change anything on airbnb.com, or only read data?

It only reads. It looks things up on airbnb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/prepare_booking, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/prepare_booking

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/prepare_booking
