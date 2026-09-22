# Edit own profile

Automatically edit own profile on linkedin.com. Update the logged-in member's own profile headline (top-card intro), via the Edit intro modal. Requires an existing headline (LinkedIn refuses to save the intro form empty).

- Site: linkedin.com
- Address: `reduck/linkedin.com/edit_own_profile`
- Updated: 2026-09-18 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/edit_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/edit_own_profile
```

## Input

- `publicId` (string, required): The logged-in member's own LinkedIn public id (the slug in linkedin.com/in/<publicId>/).
- `about` (string, optional): New About section text. Cannot be empty (LinkedIn refuses to save it blank), and the profile must already have an About section (added once via LinkedIn's own "Add about") before this can edit it. Omit to leave About unchanged. Calling with the current About text is a safe no-op.
- `headline` (string, optional): New headline text (max 220 chars). Cannot be empty. Omit to leave the headline unchanged.

## Output

- `updated` (boolean, required)
- `about` (string, optional): The About text as read back from the profile after saving (or the existing text, unchanged, for a no-op call). Present only when about was provided.
- `headline` (string, optional): The headline as read back from the profile top card after saving. Present only when headline was provided.

## FAQ

### What does "Edit own profile" do?

Update the logged-in member's own profile headline (top-card intro), via the Edit intro modal. Requires an existing headline (LinkedIn refuses to save the intro form empty).

### How do I automatically edit own profile on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/edit_own_profile

### Is there a linkedin.com API to edit own profile?

You do not need one. "Edit own profile" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: publicId. Optional: about, headline.

### What does it return?

It returns about, updated, headline.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/edit_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/edit_own_profile
