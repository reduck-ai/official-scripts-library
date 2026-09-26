# Add a note to a HubSpot contact

Automatically add a note to a HubSpot contact on app.hubspot.com. Add a note to a HubSpot contact's timeline, by contact id. Confirms the note by reloading the record and reading its timeline back: posted is true only when a new note with this text is found, and its noteId is returned. Also reports alreadyPresent — whether the same text was already among the contact's latest timeline items — so the caller can avoid duplicates. dry_run types the note into the composer and stops before saving. Finds the right account and regional host automatically.

- Site: app.hubspot.com
- Address: `reduck/app.hubspot.com/create_note_on_contact`
- Updated: 2026-09-25 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.hubspot.com/create_note_on_contact`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/create_note_on_contact
```

## Input

- `note` (string, required): The note text. Plain text.
- `contactId` (string, required): The contact's HubSpot id, as returned by the contact search (or create_or_update_contact).
- `dry_run` (boolean, optional): When true the note is typed into the composer and the run stops before saving it. Nothing is added.
- `portalId` (string, optional): The HubSpot account id, when the login has more than one. Omit it to use the default account.

## Output

- `dryRun` (boolean, required)
- `posted` (boolean, required): True only when a new note with this text was read back from the contact's timeline after a reload.
- `portalId` (string, required)
- `contactId` (string, required)
- `url` (string, optional)
- `noteId` (string | null, optional): HubSpot engagement id of the new note.
- `accountUsed` (string | null, optional)
- `alreadyPresent` (boolean, optional): Whether a note with the same text was already on the contact before this run (among the latest 20 timeline items). The run still adds a new one; the caller decides whether that is a duplicate.

## FAQ

### What does "Add a note to a HubSpot contact" do?

Add a note to a HubSpot contact's timeline, by contact id. Confirms the note by reloading the record and reading its timeline back: posted is true only when a new note with this text is found, and its noteId is returned. Also reports alreadyPresent — whether the same text was already among the contact's latest timeline items — so the caller can avoid duplicates. dry_run types the note into the composer and stops before saving. Finds the right account and regional host automatically.

### How do I automatically add a note to a HubSpot contact on app.hubspot.com?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/create_note_on_contact, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/create_note_on_contact

### Is there a app.hubspot.com API to add a note to a HubSpot contact?

You do not need one. "Add a note to a HubSpot contact" drives the real app.hubspot.com pages in a browser, so it works whether or not app.hubspot.com offers an API for this.

### What information do I need to provide?

Required: contactId, note. Optional: dry_run, portalId.

### What does it return?

It returns url, dryRun, noteId, posted, portalId, contactId, accountUsed, alreadyPresent.

### Do I need to be logged in to app.hubspot.com?

Yes. It acts as you on app.hubspot.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.hubspot.com cookies saved by the Reduck extension.

### Does it change anything on app.hubspot.com, or only read data?

It makes changes on app.hubspot.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/create_note_on_contact, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/create_note_on_contact

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.hubspot.com/create_note_on_contact
