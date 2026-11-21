# Cancel an Airbnb reservation

Automatically cancel an Airbnb reservation on airbnb.com. Cancel one of your Airbnb stay reservations by confirmation code, as the guest, in two steps. First call without confirm: it shows what you paid and the refund Airbnb grants under the reservation's cancellation policy, with a reviewHash, and changes nothing. Then call with confirm true and that reviewHash to cancel: it goes through only if the refund terms are unchanged, and returns the reservation's status afterwards. A reservation that is already cancelled, or that Airbnb no longer lets you cancel, fails with a clear error and nothing changes. The host is told at once.

- Site: airbnb.com
- Address: `reduck/airbnb.com/cancel_reservation`
- Updated: 2026-11-20 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/cancel_reservation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/cancel_reservation
```

## Input

- `code` (string, required): Reservation confirmation code, e.g. HMEZNST29K (Confirm an Airbnb booking returns it).
- `confirm` (boolean, optional): false (default) only reviews: returns what you paid, the refund, and a reviewHash, and cancels nothing. true cancels, and needs the reviewHash from the review.
- `reasonId` (string, optional): Airbnb's cancellation reason code: 101 I no longer need accommodations (default), 102 I made the reservation by accident.
- `reviewHash` (string, optional): The reviewHash a review call returned. Required with confirm: the cancellation goes through only if the refund terms still match it.

## Output

- `code` (string, required)
- `status` (string, required): The reservation's status, as Airbnb names it, e.g. ACCEPTED before or CANCELED_BY_GUEST after.
- `cancelled` (boolean, required): true only after a confirmed cancellation; false for a review.
- `reviewHash` (string, required): Hash of the reservation, reason, paid and refund shown; pass it back with confirm:true to cancel.
- `paid` (string | null, optional)
- `refund` (string | null, optional): The total refund Airbnb shows on the cancellation screen.

## FAQ

### What does "Cancel an Airbnb reservation" do?

Cancel one of your Airbnb stay reservations by confirmation code, as the guest, in two steps. First call without confirm: it shows what you paid and the refund Airbnb grants under the reservation's cancellation policy, with a reviewHash, and changes nothing. Then call with confirm true and that reviewHash to cancel: it goes through only if the refund terms are unchanged, and returns the reservation's status afterwards. A reservation that is already cancelled, or that Airbnb no longer lets you cancel, fails with a clear error and nothing changes. The host is told at once.

### How do I automatically cancel an Airbnb reservation on airbnb.com?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/cancel_reservation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/cancel_reservation

### Is there a airbnb.com API to cancel an Airbnb reservation?

You do not need one. "Cancel an Airbnb reservation" drives the real airbnb.com pages in a browser, so it works whether or not airbnb.com offers an API for this.

### What information do I need to provide?

Required: code. Optional: confirm, reasonId, reviewHash.

### What does it return?

It returns code, paid, refund, status, cancelled, reviewHash.

### Do I need to be logged in to airbnb.com?

Yes. It acts as you on airbnb.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the airbnb.com cookies saved by the Reduck extension.

### Does it change anything on airbnb.com, or only read data?

It makes changes on airbnb.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/cancel_reservation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/cancel_reservation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/cancel_reservation
