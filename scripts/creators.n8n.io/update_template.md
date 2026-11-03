# Update a template on the n8n Creator Portal

Automatically update a template on the n8n Creator Portal on creators.n8n.io. Change one of the signed-in creator's templates on the n8n Creator Portal (creators.n8n.io), by its id. It covers each step after creators.n8n.io/submit_template: finalize a submission once its AI feedback is ready (name, description, and the workflow, maybe the one the AI suggests), resubmit a template a reviewer sent back (changes_needed: the workflow must differ from the one sent before), upload a new version of a published template (workflow alone), or change its price. Pass only the fields to change. Sending a name, description or workflow puts the template under human review, which takes 3 to 5 business days. The description is Markdown in the portal's sections, each one a "## " heading: Quick overview, How it works (a numbered list), Setup (a numbered list), Requirements (a bullet list), Customization (a bullet list), Additional info. Returns the template's id, name and new review status. An account can have one template under review at a time (four for a verified creator); past that, the run fails with a clear message.

- Site: creators.n8n.io
- Address: `reduck/creators.n8n.io/update_template`
- Updated: 2026-11-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/creators.n8n.io/update_template`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/update_template
```

## Input

- `id` (integer, required): The template's id, from creators.n8n.io/list_my_templates.
- `free` (boolean, optional): true to make the template free (clears its price and purchase link).
- `name` (string, optional)
- `price` (number, optional): Price in USD. Needs purchaseUrl.
- `workflow` (object, optional): The workflow JSON as n8n exports it.
- `description` (string, optional): Markdown, in the portal's ## sections.
- `purchaseUrl` (string, optional): The https link where buyers pay. Needs price.

## Output

- `id` (integer, required)
- `reviewStatus` (string | null, required)
- `name` (string | null, optional)

## FAQ

### What does "Update a template on the n8n Creator Portal" do?

Change one of the signed-in creator's templates on the n8n Creator Portal (creators.n8n.io), by its id. It covers each step after creators.n8n.io/submit_template: finalize a submission once its AI feedback is ready (name, description, and the workflow, maybe the one the AI suggests), resubmit a template a reviewer sent back (changes_needed: the workflow must differ from the one sent before), upload a new version of a published template (workflow alone), or change its price. Pass only the fields to change. Sending a name, description or workflow puts the template under human review, which takes 3 to 5 business days. The description is Markdown in the portal's sections, each one a "## " heading: Quick overview, How it works (a numbered list), Setup (a numbered list), Requirements (a bullet list), Customization (a bullet list), Additional info. Returns the template's id, name and new review status. An account can have one template under review at a time (four for a verified creator); past that, the run fails with a clear message.

### How do I automatically update a template on the n8n Creator Portal on creators.n8n.io?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/update_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/update_template

### Is there a creators.n8n.io API to update a template on the n8n Creator Portal?

You do not need one. "Update a template on the n8n Creator Portal" drives the real creators.n8n.io pages in a browser, so it works whether or not creators.n8n.io offers an API for this.

### What information do I need to provide?

Required: id. Optional: free, name, price, workflow, description, purchaseUrl.

### What does it return?

It returns id, name, reviewStatus.

### Do I need to be logged in to creators.n8n.io?

Yes. It acts as you on creators.n8n.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the creators.n8n.io cookies saved by the Reduck extension.

### Does it change anything on creators.n8n.io, or only read data?

It makes changes on creators.n8n.io, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/update_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/update_template

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/creators.n8n.io/update_template
