# Simulate a BoursoBank personal loan

Automatically simulate a BoursoBank personal loan on boursobank.com. Run BoursoBank's personal loan simulator (prêt personnel) for an amount and a duration, without an account. Returns the monthly payment, fixed debit rate, fixed TAEG, total repaid and total interest, BoursoBank's link to apply, the discounted eco-responsible terms granted once proof is validated, and the market-average loan BoursoBank compares itself to (null when the site shows none). BoursoBank has one simulator for every project: amounts from 200 to 100 000 € and a fixed list of durations from 3 to 120 months, both returned as bounds; a request outside them fails with the allowed range.

- Site: boursobank.com
- Address: `reduck/boursobank.com/simulate-personal-loan`
- Updated: 2026-11-19 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/boursobank.com/simulate-personal-loan`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/boursobank.com/simulate-personal-loan
```

## Input

- `amount` (integer, required): Amount borrowed in euros, in steps of 100 (BoursoBank allows 200 to 100 000 €).
- `duration` (integer, required): Repayment duration in months, one of the durations BoursoBank offers.
- `project` (string, optional): No longer used: BoursoBank's simulator has one offer for every project. Accepted so older callers keep working, and echoed back.

## Output

- `url` (string, required)
- `taeg` (number, required): Fixed TAEG (annual percentage rate of charge), percent.
- `amount` (integer, required)
- `bounds` (object, required): Amount range and durations the site allows.
- `debit_rate` (number, required): Fixed annual debit rate, percent.
- `total_repaid` (number, required): Total amount due over the loan, euros.
- `market_average` (object | null, required): The market benchmark BoursoBank shows next to its offer, as the site sends it; null when the site shows none.
- `total_interest` (number, required): Total interest cost, euros.
- `duration_months` (integer, required)
- `eco_responsible` (object | null, required): Discounted terms for an eco-responsible project, granted once proof is validated; null when BoursoBank offers none.
- `monthly_payment` (number, required): Monthly instalment in euros, excluding optional insurance.
- `project` (string | null, optional)
- `subscribe_url` (string | null, optional): BoursoBank's link to start this loan application.

## FAQ

### What does "Simulate a BoursoBank personal loan" do?

Run BoursoBank's personal loan simulator (prêt personnel) for an amount and a duration, without an account. Returns the monthly payment, fixed debit rate, fixed TAEG, total repaid and total interest, BoursoBank's link to apply, the discounted eco-responsible terms granted once proof is validated, and the market-average loan BoursoBank compares itself to (null when the site shows none). BoursoBank has one simulator for every project: amounts from 200 to 100 000 € and a fixed list of durations from 3 to 120 months, both returned as bounds; a request outside them fails with the allowed range.

### How do I automatically simulate a BoursoBank personal loan on boursobank.com?

Ask an AI agent connected to Reduck to run reduck/boursobank.com/simulate-personal-loan, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boursobank.com/simulate-personal-loan

### Is there a boursobank.com API to simulate a BoursoBank personal loan?

You do not need one. "Simulate a BoursoBank personal loan" drives the real boursobank.com pages in a browser, so it works whether or not boursobank.com offers an API for this.

### What information do I need to provide?

Required: amount, duration. Optional: project.

### What does it return?

It returns url, taeg, amount, bounds, project, debit_rate, total_repaid, subscribe_url, market_average, total_interest, duration_months, eco_responsible, monthly_payment.

### Do I need to be logged in to boursobank.com?

No. It only uses pages of boursobank.com that are reachable without signing in.

### Does it change anything on boursobank.com, or only read data?

It only reads. It looks things up on boursobank.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/boursobank.com/simulate-personal-loan, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boursobank.com/simulate-personal-loan

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/boursobank.com/simulate-personal-loan
