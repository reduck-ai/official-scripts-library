# Get LinkedIn post reactors

Automatically get LinkedIn post reactors on linkedin.com. Total reaction count plus everyone in the reactions popup, with headline and connection degree.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_post_reactors`
- Updated: 2026-10-05 (v14)
- Author: Reduck AI (reduck)

## About

LinkedIn tells you a post got 240 reactions, then makes you open a small popup and scroll it by hand to see who they were. Paste the post URL and that popup comes back as rows you can filter, in LinkedIn's own order, with the total on top. The post does not have to be yours: anything your signed-in account can open works, a competitor's included. Say you sell payroll software and a rival's pricing post pulls 300 reactions. Run it with limit 300, keep the 2nd-degree people whose headline mentions HR or Payroll, and you have a short list for the connect script. Rows load by scrolling the popup, so a post with a few thousand reactions takes a good while and can stop short if LinkedIn stops loading names. Reaction type and timestamp are not in the output. Degree is relative to the signed-in account, so a colleague running the same post can get different values.

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

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "total": 3,
  "reactors": [
    {
      "name": "Example",
      "type": "…",
      "degree": "…",
      "headline": "…",
      "profileUrl": "https://example.com/item/123"
    }
  ]
}
```

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

### Can I get the reactors of someone else's LinkedIn post, or only my own?

get_post_reactors works on any LinkedIn post the signed-in account can open, a competitor's or a creator's included, since it reads the same list LinkedIn shows when you click the reaction count. LinkedIn's official Reactions API only reads reactions on posts of company pages where you are an admin or sponsored content poster, and its member-level read permission goes to select developers only.

### Can I see which reaction each person gave, like Celebrate or Insightful?

get_post_reactors tells you who reacted, not whether they picked Like, Celebrate, Insightful or another reaction, and not when. LinkedIn's Reactions API does return a reactionType and a created time for each reaction, but only on posts of a company page you manage as an admin or sponsored content poster.

### How many reactors can I pull from one LinkedIn post?

get_post_reactors returns up to 200 reactors per run by default; set limit higher for a bigger post. Fewer rows than both total and limit means LinkedIn stopped loading names into the popup (the run gives up after four scrolls in a row add nothing) or some reactors were pages other than a person or company profile, which are skipped. There is no offset, so every run starts again from the top of the list.

### Does the list include people who commented on the post?

get_post_reactors lists only the people and pages who reacted; commenters, with their comment text and replies, come from get_post_comments, so running both on one post URL covers everyone who engaged. To merge the lists, match on the memberUrn from get_profile instead of the raw profile URL, since one person can appear as /in/janedoe in one list and /in/ACoAA... in the other, and members can change their vanity URL.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_post_reactors
