# Get LinkedIn post reactors

Automatically get LinkedIn post reactors on linkedin.com. Get who reacted to a LinkedIn post from its URL: returns the post's total reaction count and the list of reactors (name, profile URL, headline, connection degree, and person vs company), in the order LinkedIn shows them. Use `limit` to cap how many reactors come back. The specific reaction type each person gave (like/celebrate/…) isn't available, and a `reactors` list shorter than `total` means your `limit` was reached.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_post_reactors`
- Updated: 2026-09-16 (v14)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_post_reactors`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post_reactors
```

## Input

- `url` (string, optional): Alias for postUrl (accepted for compatibility — prefer postUrl).
- `limit` (integer, optional): Maximum number of reactors to return. Default 200.
- `postUrl` (string, optional): The LinkedIn post's URL, e.g. https://www.linkedin.com/posts/<slug>-<id>-<code> or https://www.linkedin.com/feed/update/urn:li:activity:<id>/. Tracking/query params are fine — they're ignored.

## Output

- `total` (number, required): Total number of reactions on the post (all reaction types combined), read from the post's own reactions-count control. 0 when the post has no reactions.
- `reactors` (array, required): The reactors, in the order LinkedIn lists them, capped by `limit`. A list shorter than `total` means `limit` was reached. Empty with total 0 means the post genuinely has no reactions — confirmed by the post's action bar having rendered while no reactions-count control exists. A post that renders neither is reported as an error instead.

## FAQ

### What does "Get LinkedIn post reactors" do?

Get who reacted to a LinkedIn post from its URL: returns the post's total reaction count and the list of reactors (name, profile URL, headline, connection degree, and person vs company), in the order LinkedIn shows them. Use `limit` to cap how many reactors come back. The specific reaction type each person gave (like/celebrate/…) isn't available, and a `reactors` list shorter than `total` means your `limit` was reached.

### How do I automatically get LinkedIn post reactors on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_post_reactors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post_reactors

### Is there a linkedin.com API to get LinkedIn post reactors?

You do not need one. "Get LinkedIn post reactors" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: url, limit, postUrl.

### What does it return?

It returns total, reactors.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_post_reactors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post_reactors

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_post_reactors
