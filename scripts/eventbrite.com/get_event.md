# Get Eventbrite event details

Automatically get Eventbrite event details on eventbrite.com. Get the details of an Eventbrite event from its link or id: name, description, start and end times, venue and address or online status, organizer, ticket price range and currency, availability and sale end, status, language and image.

- Site: eventbrite.com
- Address: `reduck/eventbrite.com/get_event`
- Updated: 2026-10-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/eventbrite.com/get_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/eventbrite.com/get_event
```

## Input

- `event` (string, required): The event's Eventbrite link (any Eventbrite country site, e.g. https://www.eventbrite.com/e/...-tickets-1998255021561) or its numeric id (e.g. 1998255021561), as returned by search_events.

## Output

- `id` (string, required): Numeric event id, read from the page's canonical link. For a recurring event this is the series' main listing.
- `url` (string, required): Canonical event link.
- `name` (string, required)
- `end` (string | null, optional)
- `type` (string | null, optional): Kind of event, e.g. BusinessEvent, EducationEvent, MusicEvent.
- `image` (string | null, optional)
- `price` (object | null, optional)
- `start` (string | null, optional): ISO 8601 with the event's UTC offset.
- `venue` (object | null, optional)
- `status` (string | null, optional): e.g. EventScheduled, EventCancelled, EventPostponed.
- `isOnline` (boolean | null, optional)
- `language` (string | null, optional)
- `organizer` (object | null, optional)
- `description` (string | null, optional): Short description the organizer gave.

## FAQ

### What does "Get Eventbrite event details" do?

Get the details of an Eventbrite event from its link or id: name, description, start and end times, venue and address or online status, organizer, ticket price range and currency, availability and sale end, status, language and image.

### How do I automatically get Eventbrite event details on eventbrite.com?

Ask an AI agent connected to Reduck to run reduck/eventbrite.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eventbrite.com/get_event

### Is there a eventbrite.com API to get Eventbrite event details?

You do not need one. "Get Eventbrite event details" drives the real eventbrite.com pages in a browser, so it works whether or not eventbrite.com offers an API for this.

### What information do I need to provide?

Required: event.

### What does it return?

It returns id, end, url, name, type, image, price, start, venue, status, isOnline, language, organizer, description.

### Do I need to be logged in to eventbrite.com?

No. It only uses pages of eventbrite.com that are reachable without signing in.

### Does it change anything on eventbrite.com, or only read data?

It only reads. It looks things up on eventbrite.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/eventbrite.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eventbrite.com/get_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/eventbrite.com/get_event
