# Reveal Apollo contact email

Automatically reveal Apollo contact email on apollo.io. Reveal a person's email address on Apollo by their person id (from search_people). This adds the person to "My Prospects" and consumes an Apollo credit, same as clicking "Access email" in the UI.

- Site: apollo.io
- Address: `reduck/apollo.io/get_contact_email`
- Updated: 2026-09-01 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/apollo.io/get_contact_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/apollo.io/get_contact_email
```

## Input

- `person_id` (string, required): Apollo person id, e.g. from search_people's people[].id

## Output

- `email` (string | null, required)
- `person_id` (string, required)
- `name` (string | null, optional)

## FAQ

### What does "Reveal Apollo contact email" do?

Reveal a person's email address on Apollo by their person id (from search_people). This adds the person to "My Prospects" and consumes an Apollo credit, same as clicking "Access email" in the UI.

### How do I automatically reveal Apollo contact email on apollo.io?

Ask an AI agent connected to Reduck to run reduck/apollo.io/get_contact_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apollo.io/get_contact_email

### Is there a apollo.io API to reveal Apollo contact email?

You do not need one. "Reveal Apollo contact email" drives the real apollo.io pages in a browser, so it works whether or not apollo.io offers an API for this.

### What information do I need to provide?

Required: person_id.

### What does it return?

It returns name, email, person_id.

### Do I need to be logged in to apollo.io?

Yes. It acts as you on apollo.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the apollo.io cookies saved by the Reduck extension.

### Does it change anything on apollo.io, or only read data?

It makes changes on apollo.io, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/apollo.io/get_contact_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apollo.io/get_contact_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/apollo.io/get_contact_email
