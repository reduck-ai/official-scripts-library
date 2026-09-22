# Get Bank of America published auto loan rates

Automatically get Bank of America published auto loan rates on bankofamerica.com. Read the auto loan rates Bank of America publishes for a US state: the "as low as" APR for a new car and for a used car bought from a dealer at 60 months, the date they are effective, the term lengths the online application offers, the loan types the bank no longer offers, and the Preferred Rewards interest discounts a customer can stack on top. No account, application or credit check. These are advertised floor rates for excellent credit; a personal rate needs a Bank of America login for pre-qualification or a full application.

- Site: bankofamerica.com
- Address: `reduck/bankofamerica.com/get-auto-loan-rates`
- Updated: 2026-09-13 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bankofamerica.com/get-auto-loan-rates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bankofamerica.com/get-auto-loan-rates
```

## Input

- `state` (string, required): Two-letter US state code, e.g. CA. Bank of America keys its rate lookup on the state; the five states sampled in September 2026 returned the same APRs.

## Output

- `url` (string, required)
- `as_of` (string | null, required): The effective date shown on the page.
- `rates` (array, required): One entry per published loan type, as Bank of America names it.
- `state` (string, required)
- `discontinued` (string | null, required): Loan types the page says are no longer offered.
- `rates_timestamp` (string | null, required): Timestamp Bank of America attaches to the rate lookup.
- `rewards_discounts` (array, required): Preferred Rewards interest rate discounts by tier, in percentage points.
- `application_terms_months` (array, required): Term lengths selectable in the online application.

## FAQ

### What does "Get Bank of America published auto loan rates" do?

Read the auto loan rates Bank of America publishes for a US state: the "as low as" APR for a new car and for a used car bought from a dealer at 60 months, the date they are effective, the term lengths the online application offers, the loan types the bank no longer offers, and the Preferred Rewards interest discounts a customer can stack on top. No account, application or credit check. These are advertised floor rates for excellent credit; a personal rate needs a Bank of America login for pre-qualification or a full application.

### How do I automatically get Bank of America published auto loan rates on bankofamerica.com?

Ask an AI agent connected to Reduck to run reduck/bankofamerica.com/get-auto-loan-rates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bankofamerica.com/get-auto-loan-rates

### Is there a bankofamerica.com API to get Bank of America published auto loan rates?

You do not need one. "Get Bank of America published auto loan rates" drives the real bankofamerica.com pages in a browser, so it works whether or not bankofamerica.com offers an API for this.

### What information do I need to provide?

Required: state.

### What does it return?

It returns url, as_of, rates, state, discontinued, rates_timestamp, rewards_discounts, application_terms_months.

### Do I need to be logged in to bankofamerica.com?

No. It only uses pages of bankofamerica.com that are reachable without signing in.

### Does it change anything on bankofamerica.com, or only read data?

It only reads. It looks things up on bankofamerica.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bankofamerica.com/get-auto-loan-rates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bankofamerica.com/get-auto-loan-rates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bankofamerica.com/get-auto-loan-rates
