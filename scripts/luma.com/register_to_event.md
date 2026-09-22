# Luma API: register for a free event

Automatically register for a free event on luma.com. An unofficial Luma API for attendee registration: Luma's own API lets a host add guests to their events, not register you for someone else's, and this does that programmatically in one call. Register the signed-in Luma account for a free public event by its slug. Custom registration questions are answered from what you pass in `answers`, and a phone number from `phone_number` — nothing is invented, so an unanswered required question is refused rather than guessed at. Required terms and agreement boxes are ticked only when you pass accept_terms:true; optional marketing opt-ins are never ticked. Fails loudly on events that aren't free or aren't open for registration. This signs you up as an attendee under your real identity, so confirm the event with the person you're helping before running it — cancelling afterward is a separate action.

- Site: luma.com
- Address: `reduck/luma.com/register_to_event`
- Updated: 2026-09-18 (v22)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/register_to_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/register_to_event
```

## Input

- `slug` (string, required): The event's short Luma slug, e.g. "9n5kxo7k" from luma.com/9n5kxo7k.
- `answers` (object, optional): Answers to the event's custom registration questions, keyed by the question's id or its exact label. Takes precedence over `select_preferences` and over anything `profile` would fill. This script never invents an answer: if a required question is answered by none of them the run is refused, and a key matching no question on the event is also refused rather than silently dropped. Values: a string for text/linkedin/url questions; for a "select" question the value must be one of that question's own options verbatim (an array of them when the question allows multiple); for a "company" question either a string, or {"company": "...", "job_title": "..."}.
- `dry_run` (boolean, optional): Set true to fill the registration form and report what would be submitted, without registering: no guest list is touched and no organizer is notified. Use it to check that an event's questions are answerable, and that each value landed on the question you expect, before committing. On an event with no questions and no phone requirement there is no form to fill, because Luma's button registers on the first click, so a dry run reports the plan without clicking anything.
- `profile` (object, optional): Who is registering, so recurring questions answer themselves instead of being restated per event. Luma gives several identity questions their own type (linkedin, telegram, twitter, instagram, github, email, url), and each is filled from the matching field below by type. A question asking for one of those as plain text is matched on its label instead. It never ticks a consent box, which stays behind accept_terms, and anything it cannot map is refused rather than guessed. Run with dry_run first to see exactly which question each field landed on.
- `accept_terms` (boolean, optional): Set true to accept the event's required terms / agreement checkboxes (question_type "terms" or "agree-check") on behalf of the signed-in account. Defaults to false, and an event carrying a required one is refused without it, because agreeing to an organizer's terms is a deliberate act and not something this script will do implicitly. Optional consent boxes, typically marketing or data-sharing opt-ins, are never ticked even when this is true.
- `phone_number` (string, optional): Phone number to submit, in international format (e.g. "+33612345678"). Required only for events whose phone_number_requirement is "required" — such a run is refused without it, unless `profile.phone` supplies one. Earlier versions fabricated a random French mobile here; this script no longer invents one.
- `select_preferences` (array, optional): Option values you accept on dropdown questions, in priority order, e.g. ["AI Engineer", "R&D", "Engineering", "France", "5+ years", "Other"]. For each dropdown you have not answered in `answers`, the first entry that exactly matches one of that question's own options is used (case and surrounding spaces ignored). Nothing is invented: an entry matching no option is simply not used, and a question nothing matches is still refused. Because events word their options differently, list the variants you would accept. Check `planned` on a dry run to see which entry each question took.

## Output

- `slug` (string, required)
- `event_id` (string, required)
- `already_registered` (boolean, required)
- `dry_run` (boolean, optional): True when nothing was submitted.
- `planned` (array, optional): On a dry run: one entry per registration question, what would be sent and where it came from.
- `rsvp_id` (string | null, optional)
- `ticket_key` (string | null, optional)
- `would_register` (boolean | null, optional): On a dry run: whether a real run with these arguments would now go through.
- `approval_status` (string | null, optional)

## FAQ

### What does "Luma API: register for a free event" do?

An unofficial Luma API for attendee registration: Luma's own API lets a host add guests to their events, not register you for someone else's, and this does that programmatically in one call. Register the signed-in Luma account for a free public event by its slug. Custom registration questions are answered from what you pass in `answers`, and a phone number from `phone_number` — nothing is invented, so an unanswered required question is refused rather than guessed at. Required terms and agreement boxes are ticked only when you pass accept_terms:true; optional marketing opt-ins are never ticked. Fails loudly on events that aren't free or aren't open for registration. This signs you up as an attendee under your real identity, so confirm the event with the person you're helping before running it — cancelling afterward is a separate action.

### How do I automatically register for a free event on luma.com?

Ask an AI agent connected to Reduck to run reduck/luma.com/register_to_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/register_to_event

### Is there a luma.com API to register for a free event?

You do not need one. "Luma API: register for a free event" drives the real luma.com pages in a browser, so it works whether or not luma.com offers an API for this.

### What information do I need to provide?

Required: slug. Optional: answers, dry_run, profile, accept_terms, phone_number, select_preferences.

### What does it return?

It returns slug, dry_run, planned, rsvp_id, event_id, ticket_key, would_register, approval_status, already_registered.

### Do I need to be logged in to luma.com?

Yes. It acts as you on luma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the luma.com cookies saved by the Reduck extension.

### Does it change anything on luma.com, or only read data?

It makes changes on luma.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/register_to_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/register_to_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/register_to_event
