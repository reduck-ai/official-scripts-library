# List all cabinets

Automatically list all cabinets on barreaunantes.fr. All law firms (cabinets) in the Barreau de Nantes directory — read straight from the directory form's cabinet dropdown.

- Site: barreaunantes.fr
- Address: `reduck/barreaunantes.fr/list_cabinets`
- Updated: 2026-09-21 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/barreaunantes.fr/list_cabinets`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/barreaunantes.fr/list_cabinets
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `cabinets` (array, required)

## FAQ

### What does "List all cabinets" do?

All law firms (cabinets) in the Barreau de Nantes directory — read straight from the directory form's cabinet dropdown.

### How do I automatically list all cabinets on barreaunantes.fr?

Ask an AI agent connected to Reduck to run reduck/barreaunantes.fr/list_cabinets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/barreaunantes.fr/list_cabinets

### Is there a barreaunantes.fr API to list all cabinets?

You do not need one. "List all cabinets" drives the real barreaunantes.fr pages in a browser, so it works whether or not barreaunantes.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, cabinets.

### Do I need to be logged in to barreaunantes.fr?

No. It only uses pages of barreaunantes.fr that are reachable without signing in.

### Does it change anything on barreaunantes.fr, or only read data?

Unknown: its author has not declared whether it changes anything on barreaunantes.fr, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/barreaunantes.fr/list_cabinets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/barreaunantes.fr/list_cabinets

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/barreaunantes.fr/list_cabinets
