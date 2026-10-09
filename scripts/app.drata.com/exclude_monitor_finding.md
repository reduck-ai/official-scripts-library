# Exclude a Drata monitoring finding

Automatically exclude a Drata monitoring finding on app.drata.com. Exclude one failing resource (a repository, a person, a cloud resource) from a Drata monitoring test, with the written justification Drata shows auditors in its audit packages. Give the test page URL, the resource exactly as listed in the test's findings, and the reason. Needs a Drata session. It changes your compliance results, and undoing it is done from the test's Exclusions tab.

- Site: app.drata.com
- Address: `reduck/app.drata.com/exclude_monitor_finding`
- Updated: 2026-10-08 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.drata.com/exclude_monitor_finding`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.drata.com/exclude_monitor_finding
```

## Input

- `reason` (string, required): Justification for the exclusion, shown to auditors. Max 1000 characters.
- `testUrl` (string, required): Any URL of the Drata monitoring test page (overview, findings or exclusions tab), e.g. https://app2.drata.com/main/NA/<workspace>/1/compliance/monitoring/production/87/overview. app.drata.com links are accepted.
- `resourceName` (string, required): The resource exactly as shown in the test's findings list, e.g. a repository like my-org/my-repo or a person's username.

## Output

- `status` (string, required)
- `resourceName` (string, required)
- `verifiedOnPage` (boolean, required): True once the resource is no longer listed among the test's findings.
- `reason` (string, optional)
- `testId` (integer | null, optional)

## FAQ

### What does "Exclude a Drata monitoring finding" do?

Exclude one failing resource (a repository, a person, a cloud resource) from a Drata monitoring test, with the written justification Drata shows auditors in its audit packages. Give the test page URL, the resource exactly as listed in the test's findings, and the reason. Needs a Drata session. It changes your compliance results, and undoing it is done from the test's Exclusions tab.

### How do I automatically exclude a Drata monitoring finding on app.drata.com?

Ask an AI agent connected to Reduck to run reduck/app.drata.com/exclude_monitor_finding, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.drata.com/exclude_monitor_finding

### Is there a app.drata.com API to exclude a Drata monitoring finding?

You do not need one. "Exclude a Drata monitoring finding" drives the real app.drata.com pages in a browser, so it works whether or not app.drata.com offers an API for this.

### What information do I need to provide?

Required: testUrl, resourceName, reason.

### What does it return?

It returns reason, status, testId, resourceName, verifiedOnPage.

### Do I need to be logged in to app.drata.com?

Yes. It acts as you on app.drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.drata.com cookies saved by the Reduck extension.

### Does it change anything on app.drata.com, or only read data?

It makes changes on app.drata.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.drata.com/exclude_monitor_finding, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.drata.com/exclude_monitor_finding

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.drata.com/exclude_monitor_finding
