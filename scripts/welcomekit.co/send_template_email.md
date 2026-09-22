# Send templated email to candidate

Automatically send templated email to candidate on welcomekit.co. Send an email to an ATS candidate from a saved template, with the ATS's variable rendering and optional subject/body overrides. Returns emailId, to, subject. This sends a real email from the recruiter's account and logs it on the candidate's timeline.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/send_template_email`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/send_template_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/send_template_email
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code).
- `candidateReference` (string, required): Candidate reference from list_candidates, format: <orgprefix>-<24 hex chars>
- `templateId` (integer, optional): Template id from list_email_templates. Wins over templateName when both given.
- `bodyOverride` (string, optional): Replace the rendered body (HTML)
- `templateName` (string, optional): Template name from list_email_templates (case-insensitive exact match)
- `subjectOverride` (string, optional): Replace the rendered subject

## Output

- `emailId` (integer, required)
- `candidateReference` (string, required)
- `to` (string | null, optional): Candidate's email address
- `subject` (string | null, optional)
- `createdAt` (string | null, optional)
- `templateUsed` (string | null, optional)

## FAQ

### What does "Send templated email to candidate" do?

Send an email to an ATS candidate from a saved template, with the ATS's variable rendering and optional subject/body overrides. Returns emailId, to, subject. This sends a real email from the recruiter's account and logs it on the candidate's timeline.

### How do I automatically send templated email to candidate on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/send_template_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/send_template_email

### Is there a welcomekit.co API to send templated email to candidate?

You do not need one. "Send templated email to candidate" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org, candidateReference. Optional: templateId, bodyOverride, templateName, subjectOverride.

### What does it return?

It returns to, emailId, subject, createdAt, templateUsed, candidateReference.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It makes changes on welcomekit.co, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/send_template_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/send_template_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/send_template_email
