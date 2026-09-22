# Get LinkedIn newsletter edition reactors

Automatically get LinkedIn newsletter edition reactors on linkedin.com. Get who reacted to a LinkedIn newsletter edition from its permalink: returns the edition's total reaction count and the list of reactors (name, profile URL, headline, connection degree, and person vs company), in the order LinkedIn shows them. Use limit to cap how many reactors come back. The specific reaction type each person gave isn't available, and a reactors list shorter than total means your limit was reached.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_edition_reactors`
- Updated: 2026-09-08 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_edition_reactors`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_edition_reactors
```

## Input

- `editionUrl` (string, required): LinkedIn newsletter edition permalink, e.g. https://www.linkedin.com/pulse/<slug>-<code>/. Query string is stripped.
- `limit` (integer, optional): Maximum number of reactors to return. Default 200.

## Output

- `total` (number, required): Total number of reactions on the edition, read from its own reactions-count control.
- `reactors` (array, required): The reactors, in the order LinkedIn lists them, capped at limit. A list shorter than total means limit was reached. An empty list means the reactions-count control was not found (indistinguishable from a 0-reaction edition).

## FAQ

### What does "Get LinkedIn newsletter edition reactors" do?

Get who reacted to a LinkedIn newsletter edition from its permalink: returns the edition's total reaction count and the list of reactors (name, profile URL, headline, connection degree, and person vs company), in the order LinkedIn shows them. Use limit to cap how many reactors come back. The specific reaction type each person gave isn't available, and a reactors list shorter than total means your limit was reached.

### How do I automatically get LinkedIn newsletter edition reactors on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_edition_reactors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_edition_reactors

### Is there a linkedin.com API to get LinkedIn newsletter edition reactors?

You do not need one. "Get LinkedIn newsletter edition reactors" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: editionUrl. Optional: limit.

### What does it return?

It returns total, reactors.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_edition_reactors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_edition_reactors

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_edition_reactors
