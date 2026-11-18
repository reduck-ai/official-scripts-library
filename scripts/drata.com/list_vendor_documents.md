# List a Drata vendor's documents and security reviews

Automatically list a Drata vendor's documents and security reviews on drata.com. Lists what Drata holds for one vendor: its status, type, risk levels, sub-processor and PII flags, the documents attached to it (name, type, date added, who added it) and its security reviews. Takes the vendor's Drata id. Read-only. Requires being signed in to Drata.

- Site: drata.com
- Address: `reduck/drata.com/list_vendor_documents`
- Updated: 2026-11-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/list_vendor_documents`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/list_vendor_documents
```

## Input

- `vendorId` (integer, required): The vendor's Drata id, a number.
- `workspacePath` (string, required): The part of the Drata app URL after app2.drata.com/main/, up to and including the workspace number, e.g. NA/acme/1.

## Output

- `name` (string, required)
- `vendorId` (integer, required)
- `documents` (array, required)
- `risk` (string | null, optional)
- `type` (string | null, optional)
- `hasPii` (boolean | null, optional)
- `status` (string | null, optional)
- `impactLevel` (string | null, optional)
- `documentCount` (integer, optional)
- `isSubProcessor` (boolean | null, optional)
- `trustCenterUrl` (string | null, optional)
- `securityReviews` (array, optional)

## FAQ

### What does "List a Drata vendor's documents and security reviews" do?

Lists what Drata holds for one vendor: its status, type, risk levels, sub-processor and PII flags, the documents attached to it (name, type, date added, who added it) and its security reviews. Takes the vendor's Drata id. Read-only. Requires being signed in to Drata.

### How do I automatically list a Drata vendor's documents and security reviews on drata.com?

Ask an AI agent connected to Reduck to run reduck/drata.com/list_vendor_documents, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/list_vendor_documents

### Is there a drata.com API to list a Drata vendor's documents and security reviews?

You do not need one. "List a Drata vendor's documents and security reviews" drives the real drata.com pages in a browser, so it works whether or not drata.com offers an API for this.

### What information do I need to provide?

Required: workspacePath, vendorId.

### What does it return?

It returns name, risk, type, hasPii, status, vendorId, documents, impactLevel, documentCount, isSubProcessor, trustCenterUrl, securityReviews.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It only reads. It looks things up on drata.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/list_vendor_documents, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/list_vendor_documents

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/list_vendor_documents
