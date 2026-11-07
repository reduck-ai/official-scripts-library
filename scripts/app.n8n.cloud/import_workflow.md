# Import a workflow into n8n Cloud

Import a workflow (the JSON n8n exports) into an n8n Cloud instance as the signed-in user, as the editor does when you import a workflow from a file: n8n saves it as a new, unpublished workflow in the user's personal project, with the name the JSON gives. Returns the new workflow's id, url and name, how many nodes n8n saved, how many it skipped (a node with no type), and the node types the instance does not have installed (such nodes are saved but cannot run until their package is installed). Credentials are not part of an export, so nodes that need one must be set up in the editor. An instance that does not exist fails with a clear message.

- Site: app.n8n.cloud
- Address: `reduck/app.n8n.cloud/import_workflow`
- Updated: 2026-11-06 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.n8n.cloud/import_workflow`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.n8n.cloud/import_workflow
```

## Input

- `instance` (string, required): The instance's name: the subdomain of <instance>.app.n8n.cloud.
- `workflow` (object, required): The workflow JSON as n8n exports it (Download in the workflow menu), with its name, nodes and connections.

## Output

- `id` (string, required): The new workflow's id.
- `url` (string, required): The workflow's page in the editor.
- `name` (string, required)
- `nodeCount` (integer, required): The nodes n8n saved, sticky notes included.
- `skippedNodes` (integer, required): The nodes of the JSON that n8n did not import, for example a node with no type. 0 when it imported all of them.
- `notInstalledTypes` (array, required): The node types of the workflow that this instance does not have installed, for example a community node. Empty when every node can run.

## FAQ

### What does "Import a workflow into n8n Cloud" do?

Import a workflow (the JSON n8n exports) into an n8n Cloud instance as the signed-in user, as the editor does when you import a workflow from a file: n8n saves it as a new, unpublished workflow in the user's personal project, with the name the JSON gives. Returns the new workflow's id, url and name, how many nodes n8n saved, how many it skipped (a node with no type), and the node types the instance does not have installed (such nodes are saved but cannot run until their package is installed). Credentials are not part of an export, so nodes that need one must be set up in the editor. An instance that does not exist fails with a clear message.

### What information do I need to provide?

Required: instance, workflow.

### What does it return?

It returns id, url, name, nodeCount, skippedNodes, notInstalledTypes.

### Do I need to be logged in to app.n8n.cloud?

Yes. It acts as you on app.n8n.cloud: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.n8n.cloud cookies saved by the Reduck extension.

### Does it change anything on app.n8n.cloud, or only read data?

It makes changes on app.n8n.cloud, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.n8n.cloud/import_workflow, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.n8n.cloud/import_workflow

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.n8n.cloud/import_workflow
