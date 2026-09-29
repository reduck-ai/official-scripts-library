# Add a lead to a lemlist campaign

Automatically add a lead to a lemlist campaign on lemlist.com. Add a lead to one of your lemlist campaigns, given the campaign id (cam_... or its URL) and the lead's email. Optional fields: firstName, lastName, companyName, companyDomain, phone and linkedinUrl. Uses lemlist's own manual-add action, with no enrichment and no credits spent. Practice mode by default: it checks the campaign and tells you its name, its state, how many senders are connected, and whether the email is already a lead, without adding anything. Pass dryRun:false to add for real. The lead is confirmed by re-reading the campaign's leads. If the email is already in the campaign, it reports already_present and changes nothing, because lemlist does not modify existing campaign leads. In a launched campaign with a connected sender, a new lead enters the sequence and can be emailed, so check sendersConnected first.

- Site: lemlist.com
- Address: `reduck/lemlist.com/add_lead_to_campaign`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lemlist.com/add_lead_to_campaign`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lemlist.com/add_lead_to_campaign
```

## Input

- `email` (string, required): The lead's email address.
- `campaign` (string, required): lemlist campaign id (cam_...) or any campaign URL containing it.
- `phone` (string, optional)
- `dryRun` (boolean, optional): Practice mode (default true): checks the campaign and whether the lead is already in it, then stops. Pass false to add the lead for real. In a launched campaign with a connected sender, a new lead enters the sequence and can be emailed.
- `lastName` (string, optional)
- `firstName` (string, optional)
- `companyName` (string, optional)
- `linkedinUrl` (string, optional)
- `companyDomain` (string, optional)

## Output

- `email` (string, required)
- `dryRun` (boolean, required)
- `campaignId` (string, required)
- `state` (string | null, optional): The lead's lemlist state.
- `leadId` (string | null, optional)
- `outcome` (string, optional): inserted = new lead added; already_present = the email was already in this campaign, nothing changed (lemlist does not modify existing campaign leads).
- `verified` (boolean, optional): The lead was found in the campaign on re-read.
- `campaignName` (string | null, optional)
- `campaignState` (string | null, optional)
- `alreadyPresent` (boolean, optional): The email was already a lead in this campaign before this run.
- `sendersConnected` (integer, optional): Mailboxes/senders attached to the campaign; 0 means it cannot send.

## FAQ

### What does "Add a lead to a lemlist campaign" do?

Add a lead to one of your lemlist campaigns, given the campaign id (cam_... or its URL) and the lead's email. Optional fields: firstName, lastName, companyName, companyDomain, phone and linkedinUrl. Uses lemlist's own manual-add action, with no enrichment and no credits spent. Practice mode by default: it checks the campaign and tells you its name, its state, how many senders are connected, and whether the email is already a lead, without adding anything. Pass dryRun:false to add for real. The lead is confirmed by re-reading the campaign's leads. If the email is already in the campaign, it reports already_present and changes nothing, because lemlist does not modify existing campaign leads. In a launched campaign with a connected sender, a new lead enters the sequence and can be emailed, so check sendersConnected first.

### How do I automatically add a lead to a lemlist campaign on lemlist.com?

Ask an AI agent connected to Reduck to run reduck/lemlist.com/add_lead_to_campaign, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lemlist.com/add_lead_to_campaign

### Is there a lemlist.com API to add a lead to a lemlist campaign?

You do not need one. "Add a lead to a lemlist campaign" drives the real lemlist.com pages in a browser, so it works whether or not lemlist.com offers an API for this.

### What information do I need to provide?

Required: campaign, email. Optional: phone, dryRun, lastName, firstName, companyName, linkedinUrl, companyDomain.

### What does it return?

It returns email, state, dryRun, leadId, outcome, verified, campaignId, campaignName, campaignState, alreadyPresent, sendersConnected.

### Do I need to be logged in to lemlist.com?

Yes. It acts as you on lemlist.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the lemlist.com cookies saved by the Reduck extension.

### Does it change anything on lemlist.com, or only read data?

It makes changes on lemlist.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lemlist.com/add_lead_to_campaign, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lemlist.com/add_lead_to_campaign

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lemlist.com/add_lead_to_campaign
