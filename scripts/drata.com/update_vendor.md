# Update a Drata vendor

Automatically update a Drata vendor on drata.com. Changes fields of an existing vendor in Drata (Vendors, Current): status (e.g. bring an offboarded vendor back to Active), sub-processor and PII flags, trust center, website, privacy and terms links, services, stored data and risk levels. Only the fields you pass are changed. Takes the vendor number from its Drata page URL. Returns the vendor before and after. Requires being signed in to Drata.

- Site: drata.com
- Address: `reduck/drata.com/update_vendor`
- Updated: 2026-11-17 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/update_vendor`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/update_vendor
```

## Input

- `vendorId` (integer, required): The vendor number in its Drata page URL: .../vendors/current/<number>/overview.
- `workspacePath` (string, required): The part of the Drata app URL after app2.drata.com/main/, up to and including the workspace number, e.g. NA/acme/1.
- `url` (string, optional): Vendor website.
- `risk` (string, optional): Residual risk level.
- `hasPii` (boolean, optional): The vendor stores personally identifiable information.
- `status` (string, optional): New vendor status. ARCHIVED takes it off the current list without deleting it.
- `termsUrl` (string, optional): Vendor terms of use URL.
- `dataStored` (string, optional): What data the vendor stores or processes. Markdown is accepted.
- `privacyUrl` (string, optional): Vendor privacy policy URL.
- `impactLevel` (string, optional): Inherent risk level (impact).
- `isSubProcessor` (boolean, optional): The vendor is a sub-processor of the company's customer data.
- `trustCenterUrl` (string, optional): Vendor trust center URL.
- `servicesProvided` (string, optional): What the vendor does for the company. Markdown is accepted.

## Output

- `after` (object, required)
- `before` (object, required)
- `changed` (array, required)
- `vendorPage` (string, optional)

## FAQ

### What does "Update a Drata vendor" do?

Changes fields of an existing vendor in Drata (Vendors, Current): status (e.g. bring an offboarded vendor back to Active), sub-processor and PII flags, trust center, website, privacy and terms links, services, stored data and risk levels. Only the fields you pass are changed. Takes the vendor number from its Drata page URL. Returns the vendor before and after. Requires being signed in to Drata.

### How do I automatically update a Drata vendor on drata.com?

Ask an AI agent connected to Reduck to run reduck/drata.com/update_vendor, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/update_vendor

### Is there a drata.com API to update a Drata vendor?

You do not need one. "Update a Drata vendor" drives the real drata.com pages in a browser, so it works whether or not drata.com offers an API for this.

### What information do I need to provide?

Required: workspacePath, vendorId. Optional: url, risk, hasPii, status, termsUrl, dataStored, privacyUrl, impactLevel, isSubProcessor, trustCenterUrl, servicesProvided.

### What does it return?

It returns after, before, changed, vendorPage.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It makes changes on drata.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/update_vendor, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/update_vendor

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/update_vendor
