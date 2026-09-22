# Capture a page as a PNG

Automatically capture a page as a PNG on reddit.com. Screenshot any URL (not limited to Reddit) at a pinned viewport width and pixel density, and save it to the machine's Downloads folder as a real browser download. Runs signed in when the target host has a session, so Reddit captures have no cookie banner and no logged-out login panel. fullPage:true captures the whole scrollable page for assets that need scrolling; pass clipHeight to bound a very long page. Returns the filename, size in bytes, image width and height, and the page title. Confirmed on reddit.com: capturing while signed OUT triggers Reddit's bot detection (tab gets detached non-deterministically); once the device is actually logged into Reddit, both fullPage and viewport-only captures are clean.

- Site: reddit.com
- Address: `reduck/reddit.com/capture_page_png`
- Updated: 2026-09-18 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/capture_page_png`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/capture_page_png
```

## Input

- `url` (string, required): URL to capture.
- `filename` (string, required): Download filename, e.g. search-tall.png
- `fullPage` (boolean, optional): Capture the whole scrollable page rather than just the viewport.
- `settleMs` (number, optional): How long to let the page settle before shooting.
- `clipHeight` (number, optional): Optional CSS-px cap on captured height; useful when fullPage would be enormous.
- `viewportWidth` (number, optional): CSS viewport width to pin.
- `viewportHeight` (number, optional): CSS viewport height to pin.
- `deviceScaleFactor` (number, optional): DPR. 2 yields a 2x asset.

## Output

- `bytes` (number, optional)
- `title` (string, optional)
- `width` (number, optional)
- `height` (number, optional)
- `filename` (string, optional)
- `loggedIn` (boolean, optional)

## FAQ

### What does "Capture a page as a PNG" do?

Screenshot any URL (not limited to Reddit) at a pinned viewport width and pixel density, and save it to the machine's Downloads folder as a real browser download. Runs signed in when the target host has a session, so Reddit captures have no cookie banner and no logged-out login panel. fullPage:true captures the whole scrollable page for assets that need scrolling; pass clipHeight to bound a very long page. Returns the filename, size in bytes, image width and height, and the page title. Confirmed on reddit.com: capturing while signed OUT triggers Reddit's bot detection (tab gets detached non-deterministically); once the device is actually logged into Reddit, both fullPage and viewport-only captures are clean.

### How do I automatically capture a page as a PNG on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/capture_page_png, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/capture_page_png

### Is there a reddit.com API to capture a page as a PNG?

You do not need one. "Capture a page as a PNG" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: url, filename. Optional: fullPage, settleMs, clipHeight, viewportWidth, viewportHeight, deviceScaleFactor.

### What does it return?

It returns bytes, title, width, height, filename, loggedIn.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/capture_page_png, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/capture_page_png

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/capture_page_png
