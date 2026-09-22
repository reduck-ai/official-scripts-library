# Create a Google Workspace user (Admin console)

Automatically create a Google Workspace user (Admin console) on google.com. Creates a new user in the Google Admin console (Workspace) under the domain of the given admin account: fills first/last name, primary email local-part, optional secondary (personal) email, submits with an auto-generated 16-char password, and optionally sends the native "set your password" login-instructions email to the secondary address. Returns the created email and generated password. The admin account must already be signed in to this browser, with a session recent enough that Google does not ask to confirm the password again — when it does, the script stops before touching anything and tells you to sign in once by hand.

- Site: google.com
- Address: `reduck/google.com/admin_create_user`
- Updated: 2026-08-10 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/admin_create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/admin_create_user
```

## Input

- `lastName` (string, required)
- `firstName` (string, required)
- `adminEmail` (string, required): Already-signed-in Google Workspace admin account to select in the account chooser, e.g. admin@example.com
- `primaryEmailLocalPart` (string, required): Local part of the new user's primary email (before @), the domain is whatever is preselected for this Workspace
- `secondaryEmail` (string, optional): Personal/secondary email to register on the account and optionally send login instructions to
- `sendLoginInstructions` (boolean, optional): If true and secondaryEmail is set, sends Google's native login-instructions email (a set-your-password link, not the raw password) to secondaryEmail. Default false.

## Output

- `email` (string, required)
- `password` (string, required): Auto-generated 16-character temporary password
- `loginInstructionsSent` (boolean, required)

## FAQ

### What does "Create a Google Workspace user (Admin console)" do?

Creates a new user in the Google Admin console (Workspace) under the domain of the given admin account: fills first/last name, primary email local-part, optional secondary (personal) email, submits with an auto-generated 16-char password, and optionally sends the native "set your password" login-instructions email to the secondary address. Returns the created email and generated password. The admin account must already be signed in to this browser, with a session recent enough that Google does not ask to confirm the password again — when it does, the script stops before touching anything and tells you to sign in once by hand.

### How do I automatically create a Google Workspace user (Admin console) on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/admin_create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/admin_create_user

### Is there a google.com API to create a Google Workspace user (Admin console)?

You do not need one. "Create a Google Workspace user (Admin console)" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: adminEmail, firstName, lastName, primaryEmailLocalPart. Optional: secondaryEmail, sendLoginInstructions.

### What does it return?

It returns email, password, loginInstructionsSent.

### Do I need to be logged in to google.com?

Yes. It acts as you on google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the google.com cookies saved by the Reduck extension.

### Does it change anything on google.com, or only read data?

It makes changes on google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/admin_create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/admin_create_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/admin_create_user
