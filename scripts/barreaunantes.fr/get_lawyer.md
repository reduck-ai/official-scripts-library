# Get a lawyer's detail

Automatically get a lawyer's detail on barreaunantes.fr. One lawyer's public detail sheet from the Barreau de Nantes directory, by slug (from list_lawyers or list_lawyers_by_cabinet): name, phone, email, photo, plus the page's own labelled fields (cabinet, address, languages, dominant activities, case palais, oath date, fax). Which labelled fields appear varies per lawyer. No login required. An unknown slug throws a clear not-found error rather than returning the directory's error page as a person.

- Site: barreaunantes.fr
- Address: `reduck/barreaunantes.fr/get_lawyer`
- Updated: 2026-09-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/barreaunantes.fr/get_lawyer`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/barreaunantes.fr/get_lawyer
```

## Input

- `slug` (string, required): Lawyer slug, the last path segment of their directory URL (e.g. 'johann-abras'), as returned by list_lawyers_by_cabinet.

## Output

- `url` (string, required)
- `name` (string, required)
- `slug` (string, required)
- `details` (object, required): The page's own labelled fields, keyed by the site's French labels (verbatim). Which keys appear varies per lawyer.
- `email` (string | null, optional)
- `phone` (string | null, optional)
- `photo` (string | null, optional)
- `website` (string | null, optional)
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)

## FAQ

### What does "Get a lawyer's detail" do?

One lawyer's public detail sheet from the Barreau de Nantes directory, by slug (from list_lawyers or list_lawyers_by_cabinet): name, phone, email, photo, plus the page's own labelled fields (cabinet, address, languages, dominant activities, case palais, oath date, fax). Which labelled fields appear varies per lawyer. No login required. An unknown slug throws a clear not-found error rather than returning the directory's error page as a person.

### How do I automatically get a lawyer's detail on barreaunantes.fr?

Ask an AI agent connected to Reduck to run reduck/barreaunantes.fr/get_lawyer, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/barreaunantes.fr/get_lawyer

### Is there a barreaunantes.fr API to get a lawyer's detail?

You do not need one. "Get a lawyer's detail" drives the real barreaunantes.fr pages in a browser, so it works whether or not barreaunantes.fr offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns url, name, slug, email, phone, photo, details, website, lastName, firstName.

### Do I need to be logged in to barreaunantes.fr?

No. It only uses pages of barreaunantes.fr that are reachable without signing in.

### Does it change anything on barreaunantes.fr, or only read data?

It only reads. It looks things up on barreaunantes.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/barreaunantes.fr/get_lawyer, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/barreaunantes.fr/get_lawyer

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/barreaunantes.fr/get_lawyer
