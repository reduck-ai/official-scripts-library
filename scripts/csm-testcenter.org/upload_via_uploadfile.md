# Upload a file to CSM-Testcenter (file input)

Automatically upload a file to CSM-Testcenter (file input) on csm-testcenter.org. Uploads a file to the CSM-Testcenter file upload test page by setting it directly on the page's file input, and returns the server's confirmation of the upload (filename, size, content type, and SHA256 checksum).

- Site: csm-testcenter.org
- Address: `reduck/csm-testcenter.org/upload_via_uploadfile`
- Updated: 2026-09-18 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/csm-testcenter.org/upload_via_uploadfile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/csm-testcenter.org/upload_via_uploadfile
```

## Input

- `test-upload.pdf` (string, optional)

## Output

- `url` (string, required)
- `uploaded` (object, required): What the browser actually held when the form was submitted.
- `resultText` (string, required)
- `fields` (object, optional): The site's result table verbatim, as label to value.
- `sha256` (string | null, optional): Checksum the site computed over what it received, lowercased. Compare against the bytes sent to prove the upload arrived intact; null if the result page stopped reporting one.

## FAQ

### What does "Upload a file to CSM-Testcenter (file input)" do?

Uploads a file to the CSM-Testcenter file upload test page by setting it directly on the page's file input, and returns the server's confirmation of the upload (filename, size, content type, and SHA256 checksum).

### How do I automatically upload a file to CSM-Testcenter (file input) on csm-testcenter.org?

Ask an AI agent connected to Reduck to run reduck/csm-testcenter.org/upload_via_uploadfile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/csm-testcenter.org/upload_via_uploadfile

### Is there a csm-testcenter.org API to upload a file to CSM-Testcenter (file input)?

You do not need one. "Upload a file to CSM-Testcenter (file input)" drives the real csm-testcenter.org pages in a browser, so it works whether or not csm-testcenter.org offers an API for this.

### What information do I need to provide?

Optional: test-upload.pdf.

### What does it return?

It returns url, fields, sha256, uploaded, resultText.

### Do I need to be logged in to csm-testcenter.org?

No. It only uses pages of csm-testcenter.org that are reachable without signing in.

### Does it change anything on csm-testcenter.org, or only read data?

It makes changes on csm-testcenter.org, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/csm-testcenter.org/upload_via_uploadfile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/csm-testcenter.org/upload_via_uploadfile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/csm-testcenter.org/upload_via_uploadfile
