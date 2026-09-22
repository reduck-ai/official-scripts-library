# Leboncoin — Reply to an ad

Automatically reply to an ad on leboncoin.fr. Send a message to the seller of a Leboncoin classified ad, using the signed-in account's own contact/reply form on the ad page.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/reply_to_ad`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/reply_to_ad`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/reply_to_ad
```

## Input

- `adUrl` (string, required): Full URL of the leboncoin.fr classified ad to reply to, e.g. https://www.leboncoin.fr/ad/collection/3184559996
- `message` (string, required): The message text to send to the seller.

## Output

- `sent` (boolean, required)
- `conversationUrl` (string, required)
- `adId` (string | null, optional)

## FAQ

### What does "Leboncoin — Reply to an ad" do?

Send a message to the seller of a Leboncoin classified ad, using the signed-in account's own contact/reply form on the ad page.

### How do I automatically reply to an ad on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/reply_to_ad, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/reply_to_ad

### Is there a leboncoin.fr API to reply to an ad?

You do not need one. "Leboncoin — Reply to an ad" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Required: adUrl, message.

### What does it return?

It returns adId, sent, conversationUrl.

### Do I need to be logged in to leboncoin.fr?

Yes. It acts as you on leboncoin.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the leboncoin.fr cookies saved by the Reduck extension.

### Does it change anything on leboncoin.fr, or only read data?

It makes changes on leboncoin.fr, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/reply_to_ad, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/reply_to_ad

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/reply_to_ad
