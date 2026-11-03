# Submit a template to the n8n Creator Portal

Automatically submit a template to the n8n Creator Portal on creators.n8n.io. Submit a workflow template to the n8n Creator Portal (creators.n8n.io) as the signed-in creator, the first step of a submission: n8n runs an AI check on the workflow JSON, then waits for you to finalize. Pass the exported workflow (an object with nodes and connections, at most 15 MB), and a price with a purchase link to sell it (a verified creator only); leave both out for a free template. Returns the new template's id and review status (ai_review). The template is named "New Submission" until you finalize it: poll creators.n8n.io/get_my_template until its AI feedback is ready, then send the name and description with creators.n8n.io/update_template. An account can have one template under review at a time (four for a verified creator); past that, the run fails with a clear message.

- Site: creators.n8n.io
- Address: `reduck/creators.n8n.io/submit_template`
- Updated: 2026-11-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/creators.n8n.io/submit_template`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/submit_template
```

## Input

- `workflow` (object, required): The workflow JSON as n8n exports it (Download in the workflow menu).
- `price` (number, optional): Price in USD, to sell the template. Needs purchaseUrl. Leave out for a free template.
- `purchaseUrl` (string, optional): The https link where buyers pay. Needs price.

## Output

- `id` (integer, required)
- `reviewStatus` (string | null, required)
- `name` (string | null, optional)

## FAQ

### What does "Submit a template to the n8n Creator Portal" do?

Submit a workflow template to the n8n Creator Portal (creators.n8n.io) as the signed-in creator, the first step of a submission: n8n runs an AI check on the workflow JSON, then waits for you to finalize. Pass the exported workflow (an object with nodes and connections, at most 15 MB), and a price with a purchase link to sell it (a verified creator only); leave both out for a free template. Returns the new template's id and review status (ai_review). The template is named "New Submission" until you finalize it: poll creators.n8n.io/get_my_template until its AI feedback is ready, then send the name and description with creators.n8n.io/update_template. An account can have one template under review at a time (four for a verified creator); past that, the run fails with a clear message.

### How do I automatically submit a template to the n8n Creator Portal on creators.n8n.io?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/submit_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/submit_template

### Is there a creators.n8n.io API to submit a template to the n8n Creator Portal?

You do not need one. "Submit a template to the n8n Creator Portal" drives the real creators.n8n.io pages in a browser, so it works whether or not creators.n8n.io offers an API for this.

### What information do I need to provide?

Required: workflow. Optional: price, purchaseUrl.

### What does it return?

It returns id, name, reviewStatus.

### Do I need to be logged in to creators.n8n.io?

Yes. It acts as you on creators.n8n.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the creators.n8n.io cookies saved by the Reduck extension.

### Does it change anything on creators.n8n.io, or only read data?

It makes changes on creators.n8n.io, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/submit_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/submit_template

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/creators.n8n.io/submit_template
