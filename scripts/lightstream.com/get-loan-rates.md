# Get LightStream loan rates for a purpose, amount and term

Automatically get LightStream loan rates for a purpose, amount and term on lightstream.com. Run LightStream's rates and terms calculator for a loan purpose, amount, term in months and payment method (AutoPay or invoice), without an application or credit check. Returns the APR range and the estimated monthly payment range for that combination, the amount and term bounds LightStream accepts for the purpose, the rate date, and the full published grid of APR ranges by amount band and term band. Car financing is covered by the new_auto, used_auto_dealer, used_auto_private, lease_buyout and auto_refinance purposes. The exact rate inside the range depends on the applicant's credit profile, and invoicing runs half a point above AutoPay. Out-of-range requests fail with the allowed range.

- Site: lightstream.com
- Address: `reduck/lightstream.com/get-loan-rates`
- Updated: 2026-09-13 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lightstream.com/get-loan-rates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lightstream.com/get-loan-rates
```

## Input

- `term` (integer, required): Repayment term in months.
- `amount` (integer, required): Loan amount in US dollars.
- `purpose` (string, required): What the loan finances. Bounds depend on it; auto purposes accepted $5,000 to $100,000 over 24 to 84 months in September 2026.
- `payment_method` (string, optional): AutoPay is the quoted rate; invoicing is priced 0.50 points higher.

## Output

- `url` (string, required)
- `amount` (number, required)
- `bounds` (object, required)
- `apr_max` (number, required): Highest APR in the quoted range, percent.
- `apr_min` (number, required): Lowest APR in the quoted range, as a percentage (8.49 means 8.49%). Requires an excellent credit profile.
- `purpose` (string, required)
- `rate_table` (array, required): LightStream's published grid for this purpose and payment method: one row per amount band, one cell per term band.
- `rates_date` (string | null, required): Date the displayed rates are effective, as shown on the page.
- `disclosures` (array, required)
- `term_months` (integer, required)
- `payment_method` (string, required)
- `monthly_payment_max` (number, required): Estimated monthly payment at apr_max, US dollars.
- `monthly_payment_min` (number, required): Estimated monthly payment at apr_min, US dollars.

## FAQ

### What does "Get LightStream loan rates for a purpose, amount and term" do?

Run LightStream's rates and terms calculator for a loan purpose, amount, term in months and payment method (AutoPay or invoice), without an application or credit check. Returns the APR range and the estimated monthly payment range for that combination, the amount and term bounds LightStream accepts for the purpose, the rate date, and the full published grid of APR ranges by amount band and term band. Car financing is covered by the new_auto, used_auto_dealer, used_auto_private, lease_buyout and auto_refinance purposes. The exact rate inside the range depends on the applicant's credit profile, and invoicing runs half a point above AutoPay. Out-of-range requests fail with the allowed range.

### How do I automatically get LightStream loan rates for a purpose, amount and term on lightstream.com?

Ask an AI agent connected to Reduck to run reduck/lightstream.com/get-loan-rates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lightstream.com/get-loan-rates

### Is there a lightstream.com API to get LightStream loan rates for a purpose, amount and term?

You do not need one. "Get LightStream loan rates for a purpose, amount and term" drives the real lightstream.com pages in a browser, so it works whether or not lightstream.com offers an API for this.

### What information do I need to provide?

Required: purpose, amount, term. Optional: payment_method.

### What does it return?

It returns url, amount, bounds, apr_max, apr_min, purpose, rate_table, rates_date, disclosures, term_months, payment_method, monthly_payment_max, monthly_payment_min.

### Do I need to be logged in to lightstream.com?

No. It only uses pages of lightstream.com that are reachable without signing in.

### Does it change anything on lightstream.com, or only read data?

It only reads. It looks things up on lightstream.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lightstream.com/get-loan-rates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lightstream.com/get-loan-rates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lightstream.com/get-loan-rates
