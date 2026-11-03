# Cancel Doctolib appointment

Automatically cancel Doctolib appointment on doctolib.fr. Cancel an upcoming Doctolib appointment of the signed-in account by its id, as Book Doctolib appointment or List Doctolib appointments return it, and confirm on Doctolib that it is canceled. Returns the appointment as Doctolib shows it afterwards. It fails with a clear message when the id is not an upcoming appointment of this account (past, already canceled, or of another account), or when Doctolib no longer lets it be canceled online because it is too close; then the result names the practice's phone number when Doctolib shows one.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/cancel_appointment`
- Updated: 2026-11-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/cancel_appointment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/cancel_appointment
```

## Input

- `appointment_id` (string, required): Appointment id from book_appointment or list_appointments.

## Output

- `appointment` (object, required)

## FAQ

### What does "Cancel Doctolib appointment" do?

Cancel an upcoming Doctolib appointment of the signed-in account by its id, as Book Doctolib appointment or List Doctolib appointments return it, and confirm on Doctolib that it is canceled. Returns the appointment as Doctolib shows it afterwards. It fails with a clear message when the id is not an upcoming appointment of this account (past, already canceled, or of another account), or when Doctolib no longer lets it be canceled online because it is too close; then the result names the practice's phone number when Doctolib shows one.

### How do I automatically cancel Doctolib appointment on doctolib.fr?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/cancel_appointment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/cancel_appointment

### Is there a doctolib.fr API to cancel Doctolib appointment?

You do not need one. "Cancel Doctolib appointment" drives the real doctolib.fr pages in a browser, so it works whether or not doctolib.fr offers an API for this.

### What information do I need to provide?

Required: appointment_id.

### What does it return?

It returns appointment.

### Do I need to be logged in to doctolib.fr?

Yes. It acts as you on doctolib.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the doctolib.fr cookies saved by the Reduck extension.

### Does it change anything on doctolib.fr, or only read data?

It makes changes on doctolib.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/cancel_appointment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/cancel_appointment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/doctolib.fr/cancel_appointment
