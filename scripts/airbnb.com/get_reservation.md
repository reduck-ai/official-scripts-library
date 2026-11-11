# Get an Airbnb reservation

Automatically get an Airbnb reservation on airbnb.com. Read one of your Airbnb stay reservations by confirmation code, as the guest: the listing (room id, title, type), the host, check-in and checkout dates and times, the address and coordinates, the number of guests, the check-in method, the host's directions, the house rules and the host's requests, the house manual, the checkout instructions (the checkout time and the host's checkout requests, such as taking out the trash or starting the dishwasher, or none), the cancellation policy summary and the total cost. Text the host wrote comes in the language the host wrote it, or in Airbnb's English translation with translate. Cancel an Airbnb reservation takes the same code. A code that is not one of your reservations fails with an error that says so.

- Site: airbnb.com
- Address: `reduck/airbnb.com/get_reservation`
- Updated: 2026-11-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/get_reservation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_reservation
```

## Input

- `code` (string, required): Reservation confirmation code, e.g. HMEZNST29K. It is in the trip's page on Airbnb and in the booking email; Confirm an Airbnb booking returns it.
- `translate` (boolean, optional): True to get the text the host wrote (rules, requests, manual, directions) in Airbnb's English translation; false (default) for the host's own words.

## Output

- `code` (string, required)
- `lat` (number | null, optional)
- `lng` (number | null, optional)
- `host` (object, optional)
- `title` (string | null, optional): The stay's title, e.g. Home in Munich.
- `guests` (integer | null, optional)
- `status` (string | null, optional): The reservation's status as Airbnb names it, e.g. ACCEPT for a confirmed stay.
- `address` (string | null, optional)
- `room_id` (string | null, optional): The listing's room id, as Get Airbnb listing takes it.
- `check_in` (object, optional)
- `checkout` (object, optional)
- `timezone` (string | null, optional): The listing's IANA time zone, e.g. Europe/Berlin.
- `house_rules` (array, optional): The house rules and requests, in Airbnb's sections: the rules (guests, pets, smoking, events...) and the host's own requests for the stay.
- `house_manual` (string | null, optional): The house manual in full; null when the host wrote none.
- `listing_type` (string | null, optional): e.g. Entire rental unit in Munich.
- `check_in_method` (string | null, optional): e.g. Host greets you, Self check-in with lockbox.
- `host_directions` (string | null, optional): How to get there, as the host wrote it; null when the host wrote none.
- `payment_summary` (string | null, optional): e.g. Total cost: €735.50, in the currency paid.
- `cancellation_policy` (string | null, optional): Airbnb's summary of what a cancellation refunds now, e.g. This reservation is non-refundable.
- `checkout_instructions` (object, optional)

## FAQ

### What does "Get an Airbnb reservation" do?

Read one of your Airbnb stay reservations by confirmation code, as the guest: the listing (room id, title, type), the host, check-in and checkout dates and times, the address and coordinates, the number of guests, the check-in method, the host's directions, the house rules and the host's requests, the house manual, the checkout instructions (the checkout time and the host's checkout requests, such as taking out the trash or starting the dishwasher, or none), the cancellation policy summary and the total cost. Text the host wrote comes in the language the host wrote it, or in Airbnb's English translation with translate. Cancel an Airbnb reservation takes the same code. A code that is not one of your reservations fails with an error that says so.

### How do I automatically get an Airbnb reservation on airbnb.com?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/get_reservation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_reservation

### Is there a airbnb.com API to get an Airbnb reservation?

You do not need one. "Get an Airbnb reservation" drives the real airbnb.com pages in a browser, so it works whether or not airbnb.com offers an API for this.

### What information do I need to provide?

Required: code. Optional: translate.

### What does it return?

It returns lat, lng, code, host, title, guests, status, address, room_id, check_in, checkout, timezone, house_rules, house_manual, listing_type, check_in_method, host_directions, payment_summary, cancellation_policy, checkout_instructions.

### Do I need to be logged in to airbnb.com?

Yes. It acts as you on airbnb.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the airbnb.com cookies saved by the Reduck extension.

### Does it change anything on airbnb.com, or only read data?

It only reads. It looks things up on airbnb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/get_reservation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_reservation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/get_reservation
