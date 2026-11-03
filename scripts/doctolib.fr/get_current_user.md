# Get current Doctolib user

Automatically get current Doctolib user on doctolib.fr. Report which Doctolib patient account this browser is signed in as: the account holder's name and email. When the browser is signed out, the run fails with a signed-out error that says to sign in to Doctolib. Same answer as Doctolib whoami.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/get_current_user`
- Updated: 2026-11-02 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/get_current_user
```

## Input

It takes no input.

## Output

- `name` (string | null, required): The account holder's name.
- `email` (string | null, required): The account's email.
- `loggedIn` (boolean, required): Always true: a signed-out browser fails with a signed-out error.

## FAQ

### What does "Get current Doctolib user" do?

Report which Doctolib patient account this browser is signed in as: the account holder's name and email. When the browser is signed out, the run fails with a signed-out error that says to sign in to Doctolib. Same answer as Doctolib whoami.

### How do I automatically get current Doctolib user on doctolib.fr?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/get_current_user

### Is there a doctolib.fr API to get current Doctolib user?

You do not need one. "Get current Doctolib user" drives the real doctolib.fr pages in a browser, so it works whether or not doctolib.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to doctolib.fr?

Yes. It acts as you on doctolib.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the doctolib.fr cookies saved by the Reduck extension.

### Does it change anything on doctolib.fr, or only read data?

It only reads. It looks things up on doctolib.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/doctolib.fr/get_current_user
