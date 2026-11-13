# Get Doctolib practitioner

Automatically get Doctolib practitioner on doctolib.fr. Fetch a Doctolib practitioner's full profile from their profile_path. Returns name, specialty, bio, phone, fees, payment_means, languages, formations, experience, legals (RPPS/ADELI), and addresses with structured opening_hours.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/get_practitioner`
- Updated: 2026-11-12 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/get_practitioner`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/get_practitioner
```

## Input

- `profile_path` (string, required): Relative path or full profile URL, from search_practitioners (with ?pid=practice-N, e.g. 'medecin-generaliste/paris/prenom-nom?pid=practice-12345') or from suggest (without a pid). Every address of the practitioner is returned either way.

## Output

- `name` (string | null, required)
- `specialty` (string | null, required)
- `profile_path` (string, required)
- `bio` (string | null, optional)
- `fees` (array, optional)
- `phone` (string | null, optional)
- `legals` (object, optional)
- `bookable` (boolean | null, optional): Doctolib offers online booking on this profile (it shows its booking card).
- `addresses` (array, optional)
- `languages` (array, optional)
- `experience` (array, optional)
- `formations` (array, optional)
- `profile_id` (integer | null, optional)
- `telehealth` (boolean, optional)
- `payment_means` (array, optional)

## FAQ

### What does "Get Doctolib practitioner" do?

Fetch a Doctolib practitioner's full profile from their profile_path. Returns name, specialty, bio, phone, fees, payment_means, languages, formations, experience, legals (RPPS/ADELI), and addresses with structured opening_hours.

### How do I automatically get Doctolib practitioner on doctolib.fr?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/get_practitioner, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/get_practitioner

### Is there a doctolib.fr API to get Doctolib practitioner?

You do not need one. "Get Doctolib practitioner" drives the real doctolib.fr pages in a browser, so it works whether or not doctolib.fr offers an API for this.

### What information do I need to provide?

Required: profile_path.

### What does it return?

It returns bio, fees, name, phone, legals, bookable, addresses, languages, specialty, experience, formations, profile_id, telehealth, profile_path, payment_means.

### Do I need to be logged in to doctolib.fr?

No. It only uses pages of doctolib.fr that are reachable without signing in.

### Does it change anything on doctolib.fr, or only read data?

It only reads. It looks things up on doctolib.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/get_practitioner, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/get_practitioner

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/doctolib.fr/get_practitioner
