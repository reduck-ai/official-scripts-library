# Find Doctolib practitioners by name

Automatically find Doctolib practitioners by name on doctolib.fr. Look up a practitioner, a medical center or a specialty by name on Doctolib, as the site's search bar suggests them while you type (e.g. "Laurent Coiffier", "Clinique du Mousseau", "dermato"). Returns profiles (practitioners and organizations, with speciality, city and profile_path) and specialities (slug and name). profile_path goes straight into list_slots and get_practitioner; a speciality slug goes into search_practitioners. A query with no match returns two empty lists. Doctolib returns at most about 30 profiles and 10 specialities, with no paging: add a first name or a city word to narrow a common name.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/suggest`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/suggest`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/suggest
```

## Input

- `query` (string, required): Free text as typed in Doctolib's search bar: a practitioner's name ("Coiffier", "Laurent Coiffier"), an organization's name, or a specialty word.

## Output

- `query` (string, required)
- `profiles` (array, required): Practitioners and organizations whose name matches, in Doctolib's order.
- `specialities` (array, required): Specialties and care types whose name matches.

## FAQ

### What does "Find Doctolib practitioners by name" do?

Look up a practitioner, a medical center or a specialty by name on Doctolib, as the site's search bar suggests them while you type (e.g. "Laurent Coiffier", "Clinique du Mousseau", "dermato"). Returns profiles (practitioners and organizations, with speciality, city and profile_path) and specialities (slug and name). profile_path goes straight into list_slots and get_practitioner; a speciality slug goes into search_practitioners. A query with no match returns two empty lists. Doctolib returns at most about 30 profiles and 10 specialities, with no paging: add a first name or a city word to narrow a common name.

### How do I automatically find Doctolib practitioners by name on doctolib.fr?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/suggest, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/suggest

### Is there a doctolib.fr API to find Doctolib practitioners by name?

You do not need one. "Find Doctolib practitioners by name" drives the real doctolib.fr pages in a browser, so it works whether or not doctolib.fr offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns query, profiles, specialities.

### Do I need to be logged in to doctolib.fr?

No. It only uses pages of doctolib.fr that are reachable without signing in.

### Does it change anything on doctolib.fr, or only read data?

It only reads. It looks things up on doctolib.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/suggest, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/suggest

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/doctolib.fr/suggest
