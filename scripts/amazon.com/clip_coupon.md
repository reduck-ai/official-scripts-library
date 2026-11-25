# Clip Amazon coupon

Clip the coupon shown on an Amazon.com product page, by ASIN, on a signed-in browser: it ticks the coupon box next to the price, so the saving applies at checkout. Returns the coupon as the page shows it after the clip (for example "$3.70 coupon applied") and whether it was already clipped. A product whose page shows no coupon fails with an error that says so. Clipping orders nothing and spends nothing.

- Site: amazon.com
- Address: `reduck/amazon.com/clip_coupon`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/clip_coupon`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/clip_coupon
```

## Input

- `asin` (string, required): Product ASIN, the 10 characters after /dp/ in the product URL, e.g. B0013OUNK4.

## Output

- `asin` (string, required)
- `coupon` (string, required): The applied coupon's text as the page shows it, e.g. "$3.70 coupon applied Limit 1 item."
- `clipped` (boolean, required): True when the page shows the coupon as applied after the run.
- `already_clipped` (boolean, required): True when the coupon was already applied before this run, so nothing was clicked.

## FAQ

### What does "Clip Amazon coupon" do?

Clip the coupon shown on an Amazon.com product page, by ASIN, on a signed-in browser: it ticks the coupon box next to the price, so the saving applies at checkout. Returns the coupon as the page shows it after the clip (for example "$3.70 coupon applied") and whether it was already clipped. A product whose page shows no coupon fails with an error that says so. Clipping orders nothing and spends nothing.

### What information do I need to provide?

Required: asin.

### What does it return?

It returns asin, coupon, clipped, already_clipped.

### Do I need to be logged in to amazon.com?

Yes. It acts as you on amazon.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.com.

### Does it change anything on amazon.com, or only read data?

It makes changes on amazon.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/clip_coupon, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/clip_coupon

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/clip_coupon
