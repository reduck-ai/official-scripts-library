# DocuSign — place signature fields on a draft

Find where signatures and dates belong across every page of a DocuSign draft's document and place Sign Here and Date Signed fields there. Each spot is matched to the party who fills it (Client, Provider, Witness…), so a person who signs several times gets all of their spots; give signers a role to match explicitly. The draft is saved, never sent, and a dry run only reports the spots it found. Signed out is a clear error.

- Site: docusign.com
- Address: `reduck/docusign.com/place_signature_fields`
- Updated: 2026-09-30 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docusign.com/place_signature_fields`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docusign.com/place_signature_fields
```

## Input

- `signers` (array, required): Who signs. Give each a role matching the document's wording (e.g. "Client", "Tenant", "Witness") to match explicitly; without roles, signers are matched to the document's parties in the order each party first appears. Every signature spot of a party goes to the same signer.
- `envelopeId` (string, required): Id of the draft envelope (e.g. from docusign.com/upload_document).
- `dryRun` (boolean, optional): Only detect and return the spots; add no recipients or fields.
- `includeDates` (boolean, optional): Also place a Date Signed field on each date line belonging to a signer's party.

## Output

- `dryRun` (boolean, required)
- `placed` (array, required)
- `detected` (array, required)
- `envelopeId` (string, required)
- `parties` (array, optional)
- `signersWithoutSpot` (array, optional)
- `unassignedSignatureSpots` (integer, optional)

## FAQ

### What does "DocuSign — place signature fields on a draft" do?

Find where signatures and dates belong across every page of a DocuSign draft's document and place Sign Here and Date Signed fields there. Each spot is matched to the party who fills it (Client, Provider, Witness…), so a person who signs several times gets all of their spots; give signers a role to match explicitly. The draft is saved, never sent, and a dry run only reports the spots it found. Signed out is a clear error.

### What information do I need to provide?

Required: envelopeId, signers. Optional: dryRun, includeDates.

### What does it return?

It returns dryRun, placed, parties, detected, envelopeId, signersWithoutSpot, unassignedSignatureSpots.

### Do I need to be logged in to docusign.com?

Yes. It acts as you on docusign.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docusign.com cookies saved by the Reduck extension.

### Does it change anything on docusign.com, or only read data?

It makes changes on docusign.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docusign.com/place_signature_fields, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docusign.com/place_signature_fields

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docusign.com/place_signature_fields
