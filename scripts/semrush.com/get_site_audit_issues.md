# Get Semrush Site Audit errors and warnings

Automatically get Semrush Site Audit errors and warnings on semrush.com. List every error, warning and notice from the latest Semrush Site Audit of a project, with how many times each issue occurs. Pass a project id, or omit it to use your first Site Audit project.

- Site: semrush.com
- Address: `reduck/semrush.com/get_site_audit_issues`
- Updated: 2026-10-06 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/semrush.com/get_site_audit_issues`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/semrush.com/get_site_audit_issues
```

## Input

- `projectId` (integer, optional): Semrush project (Site Audit campaign) id, as in /siteaudit/campaign/<id>/. Omit to use the first Site Audit project.
- `includeNotices` (boolean, optional): Also return notices (lowest severity). Default true.

## Output

- `issues` (array, required)
- `totals` (object, required)
- `projectId` (integer, required)
- `domain` (string | null, optional)
- `status` (string | null, optional)
- `pagesLimit` (integer | null, optional)
- `lastAuditAt` (string | null, optional)
- `pagesCrawled` (integer | null, optional)

## FAQ

### What does "Get Semrush Site Audit errors and warnings" do?

List every error, warning and notice from the latest Semrush Site Audit of a project, with how many times each issue occurs. Pass a project id, or omit it to use your first Site Audit project.

### How do I automatically get Semrush Site Audit errors and warnings on semrush.com?

Ask an AI agent connected to Reduck to run reduck/semrush.com/get_site_audit_issues, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/semrush.com/get_site_audit_issues

### Is there a semrush.com API to get Semrush Site Audit errors and warnings?

You do not need one. "Get Semrush Site Audit errors and warnings" drives the real semrush.com pages in a browser, so it works whether or not semrush.com offers an API for this.

### What information do I need to provide?

Optional: projectId, includeNotices.

### What does it return?

It returns domain, issues, status, totals, projectId, pagesLimit, lastAuditAt, pagesCrawled.

### Do I need to be logged in to semrush.com?

Yes. It acts as you on semrush.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the semrush.com cookies saved by the Reduck extension.

### Does it change anything on semrush.com, or only read data?

It only reads. It looks things up on semrush.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/semrush.com/get_site_audit_issues, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/semrush.com/get_site_audit_issues

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/semrush.com/get_site_audit_issues
