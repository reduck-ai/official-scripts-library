# Cancel an Airbnb reservation

Automatically cancel an Airbnb reservation on airbnb.com. Cancel one of your Airbnb stay reservations by confirmation code, as the guest. Returns the refund Airbnb grants under the reservation's cancellation policy (what you paid, what comes back) and the reservation's status afterwards. A reservation that is already cancelled, or that Airbnb no longer lets you cancel, fails with a clear error and nothing changes. The host is told at once.

- Site: airbnb.com
- Address: `reduck/airbnb.com/cancel_reservation`
- Updated: 2026-10-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/cancel_reservation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/cancel_reservation
```

## Input

- `code` (string, required): Reservation confirmation code, e.g. HMEZNST29K (Confirm an Airbnb booking returns it).
- `reasonId` (string, optional): Airbnb's cancellation reason code: 101 I no longer need accommodations (default), 102 I made the reservation by accident.

## Output

- `code` (string, required)
- `status` (string, required): The reservation's status after the request, as Airbnb names it, e.g. CANCELED_BY_GUEST.
- `paid` (string | null, optional)
- `refund` (string | null, optional): The total refund Airbnb showed before confirming.

## FAQ

### What does "Cancel an Airbnb reservation" do?

Cancel one of your Airbnb stay reservations by confirmation code, as the guest. Returns the refund Airbnb grants under the reservation's cancellation policy (what you paid, what comes back) and the reservation's status afterwards. A reservation that is already cancelled, or that Airbnb no longer lets you cancel, fails with a clear error and nothing changes. The host is told at once.

### How do I automatically cancel an Airbnb reservation on airbnb.com?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/cancel_reservation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/cancel_reservation

### Is there a airbnb.com API to cancel an Airbnb reservation?

You do not need one. "Cancel an Airbnb reservation" drives the real airbnb.com pages in a browser, so it works whether or not airbnb.com offers an API for this.

### What information do I need to provide?

Required: code. Optional: reasonId.

### What does it return?

It returns code, paid, refund, status.

### Do I need to be logged in to airbnb.com?

Yes. It acts as you on airbnb.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the airbnb.com cookies saved by the Reduck extension.

### Does it change anything on airbnb.com, or only read data?

It makes changes on airbnb.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/cancel_reservation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/cancel_reservation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/cancel_reservation
