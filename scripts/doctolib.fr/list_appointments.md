# List Doctolib appointments

Automatically list Doctolib appointments on doctolib.fr. List the appointments of the signed-in Doctolib account, upcoming or past, as the account's appointments page shows them. Each appointment has its id (the one Cancel Doctolib appointment takes), start and end date, practitioner, speciality, profile path, visit motive, patient, and whether it is confirmed, canceled, past or a no-show. Past appointments come 10 at a time, newest first: pass next_cursor back as cursor for the next ones, until it comes back null. Doctolib removes old appointments from the history after some years. No appointment returns an empty list.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/list_appointments`
- Updated: 2026-11-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/list_appointments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/list_appointments
```

## Input

- `past` (boolean, optional): false: upcoming appointments. true: past appointments, newest first.
- `cursor` (string, optional): next_cursor of the previous call with the same past value, to read the next page.

## Output

- `next_cursor` (string | null, required): Pass as cursor for the next page; null on the last page.
- `appointments` (array, required)

## FAQ

### What does "List Doctolib appointments" do?

List the appointments of the signed-in Doctolib account, upcoming or past, as the account's appointments page shows them. Each appointment has its id (the one Cancel Doctolib appointment takes), start and end date, practitioner, speciality, profile path, visit motive, patient, and whether it is confirmed, canceled, past or a no-show. Past appointments come 10 at a time, newest first: pass next_cursor back as cursor for the next ones, until it comes back null. Doctolib removes old appointments from the history after some years. No appointment returns an empty list.

### How do I automatically list Doctolib appointments on doctolib.fr?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/list_appointments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/list_appointments

### Is there a doctolib.fr API to list Doctolib appointments?

You do not need one. "List Doctolib appointments" drives the real doctolib.fr pages in a browser, so it works whether or not doctolib.fr offers an API for this.

### What information do I need to provide?

Optional: past, cursor.

### What does it return?

It returns next_cursor, appointments.

### Do I need to be logged in to doctolib.fr?

Yes. It acts as you on doctolib.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the doctolib.fr cookies saved by the Reduck extension.

### Does it change anything on doctolib.fr, or only read data?

It only reads. It looks things up on doctolib.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/list_appointments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/list_appointments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/doctolib.fr/list_appointments
