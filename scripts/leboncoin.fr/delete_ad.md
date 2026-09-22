# Delete a leboncoin classified ad

Automatically delete a leboncoin classified ad on leboncoin.fr. Delete one of your own leboncoin classified ads, matched by its exact title. Confirms only against a dialog that names that ad, and reports the ad as deleted only once it has actually left the ads list. Refuses while an ad is still under review, which is when leboncoin offers no delete control.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/delete_ad`
- Updated: 2026-09-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/delete_ad`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/delete_ad
```

## Input

- `title` (string, required): Exact title of the ad to delete.

## Output

- `found` (boolean, required): Whether an ad with this title was listed before the attempt.
- `title` (string, required)
- `deleted` (boolean, required): True only when the ad is absent from a cache-busted reload afterwards.
- `dialogNamed` (string | null, optional): The ad the confirmation dialog said it was about, used to guard the shared delete control.

## FAQ

### What does "Delete a leboncoin classified ad" do?

Delete one of your own leboncoin classified ads, matched by its exact title. Confirms only against a dialog that names that ad, and reports the ad as deleted only once it has actually left the ads list. Refuses while an ad is still under review, which is when leboncoin offers no delete control.

### How do I automatically delete a leboncoin classified ad on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/delete_ad, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/delete_ad

### Is there a leboncoin.fr API to delete a leboncoin classified ad?

You do not need one. "Delete a leboncoin classified ad" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Required: title.

### What does it return?

It returns found, title, deleted, dialogNamed.

### Do I need to be logged in to leboncoin.fr?

Yes. It acts as you on leboncoin.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the leboncoin.fr cookies saved by the Reduck extension.

### Does it change anything on leboncoin.fr, or only read data?

It makes changes on leboncoin.fr, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/delete_ad, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/delete_ad

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/delete_ad
