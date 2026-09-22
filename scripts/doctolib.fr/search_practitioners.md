# Search Doctolib practitioners

Automatically search Doctolib practitioners on doctolib.fr. Search Doctolib practitioners by specialty and location. Returns total, page, and providers with full_name, specialty, address, sector, payment_means, languages, telehealth, online_booking, matched_visit_motive, and profile_path. There are 20 providers per page and the order is server-ranked; profile_path (including ?pid=practice-N) is the join key for get_practitioner and list_slots.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/search_practitioners`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/search_practitioners`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/search_practitioners
```

## Input

- `location` (string, required): City slug or name resolved by Doctolib (e.g. 'paris', 'lyon').
- `specialty` (string, required): Specialty/keyword slug or free text (e.g. 'medecin-generaliste', 'dentiste', 'dermatologue').
- `page` (integer, optional): 0-based page. Doctolib serves 20 providers per page. Default 0. Page>0 replays the page's own resolved search body against ?page=N (order is server-ranked; treat as stable within a session).

## Output

- `page` (integer, required)
- `total` (integer | null, required): Total matching providers across all pages.
- `providers` (array, required)

## FAQ

### What does "Search Doctolib practitioners" do?

Search Doctolib practitioners by specialty and location. Returns total, page, and providers with full_name, specialty, address, sector, payment_means, languages, telehealth, online_booking, matched_visit_motive, and profile_path. There are 20 providers per page and the order is server-ranked; profile_path (including ?pid=practice-N) is the join key for get_practitioner and list_slots.

### How do I automatically search Doctolib practitioners on doctolib.fr?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/search_practitioners, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/search_practitioners

### Is there a doctolib.fr API to search Doctolib practitioners?

You do not need one. "Search Doctolib practitioners" drives the real doctolib.fr pages in a browser, so it works whether or not doctolib.fr offers an API for this.

### What information do I need to provide?

Required: specialty, location. Optional: page.

### What does it return?

It returns page, total, providers.

### Do I need to be logged in to doctolib.fr?

No. It only uses pages of doctolib.fr that are reachable without signing in.

### Does it change anything on doctolib.fr, or only read data?

Unknown: its author has not declared whether it changes anything on doctolib.fr, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/search_practitioners, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/search_practitioners

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/doctolib.fr/search_practitioners
