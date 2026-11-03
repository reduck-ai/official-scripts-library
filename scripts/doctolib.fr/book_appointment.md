# Book Doctolib appointment

Automatically book Doctolib appointment on doctolib.fr. Book a Doctolib appointment for the signed-in account holder: one practitioner practice, one visit motive and one slot, as List Doctolib slots returns them. By default it stops at Doctolib's checkout without booking: Doctolib then holds the slot for 15 minutes in this browser, and the result shows the practitioner, address, motive, patient, price and the questions Doctolib asks before it books. With confirm set to true it books the slot and returns the appointment, whose id Cancel Doctolib appointment takes. A run with confirm true within those 15 minutes books the held slot. Doctolib asks some practitioners' patients whether they have consulted before: pass new_patient for those. It fails with a clear message when the slot is no longer free, when another booking is still held in this browser, or when the practitioner asks questions this script cannot answer.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/book_appointment`
- Updated: 2026-11-02 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/book_appointment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/book_appointment
```

## Input

- `motive_id` (integer, required): Visit motive id, from list_slots.visit_motives.
- `start_date` (string, required): Slot start, exactly as list_slots returns it, e.g. 2027-01-07T12:30:00.000+01:00.
- `profile_path` (string, required): Profile path with ?pid=practice-N, from search_practitioners or list_slots.
- `confirm` (boolean, optional): false: stop at checkout, the slot held for 15 minutes. true: book the slot.
- `new_patient` (boolean, optional): true when the patient has never consulted this practitioner. Needed only when Doctolib asks (asks_new_patient in the checkout result).

## Output

- `stage` (string, required)
- `questions` (array, required): Other required questions Doctolib asks before it books. The script cannot answer them, so a booking with questions fails.
- `start_date` (string, required): Slot the checkout holds.
- `appointment` (object | null, required): The booked appointment (stage booked); null at checkout.
- `asks_new_patient` (boolean, required): Doctolib asks whether the patient has consulted this practitioner before: pass new_patient.
- `price` (string | number | null, optional): Amount to pay at booking, when Doctolib asks for one.
- `motive` (object | null, optional)
- `address` (string | null, optional)
- `patient` (string | null, optional): The account holder the appointment is for.
- `telehealth` (boolean, optional)
- `practitioner` (string | null, optional)
- `profile_path` (string | null, optional)

## FAQ

### What does "Book Doctolib appointment" do?

Book a Doctolib appointment for the signed-in account holder: one practitioner practice, one visit motive and one slot, as List Doctolib slots returns them. By default it stops at Doctolib's checkout without booking: Doctolib then holds the slot for 15 minutes in this browser, and the result shows the practitioner, address, motive, patient, price and the questions Doctolib asks before it books. With confirm set to true it books the slot and returns the appointment, whose id Cancel Doctolib appointment takes. A run with confirm true within those 15 minutes books the held slot. Doctolib asks some practitioners' patients whether they have consulted before: pass new_patient for those. It fails with a clear message when the slot is no longer free, when another booking is still held in this browser, or when the practitioner asks questions this script cannot answer.

### How do I automatically book Doctolib appointment on doctolib.fr?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/book_appointment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/book_appointment

### Is there a doctolib.fr API to book Doctolib appointment?

You do not need one. "Book Doctolib appointment" drives the real doctolib.fr pages in a browser, so it works whether or not doctolib.fr offers an API for this.

### What information do I need to provide?

Required: profile_path, motive_id, start_date. Optional: confirm, new_patient.

### What does it return?

It returns price, stage, motive, address, patient, questions, start_date, telehealth, appointment, practitioner, profile_path, asks_new_patient.

### Do I need to be logged in to doctolib.fr?

Yes. It acts as you on doctolib.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the doctolib.fr cookies saved by the Reduck extension.

### Does it change anything on doctolib.fr, or only read data?

It makes changes on doctolib.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/book_appointment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/book_appointment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/doctolib.fr/book_appointment
