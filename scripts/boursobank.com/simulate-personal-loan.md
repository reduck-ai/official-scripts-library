# Simulate a BoursoBank personal loan

Automatically simulate a BoursoBank personal loan on boursobank.com. Run BoursoBank's personal loan simulator (prêt personnel) for a project type, an amount and a duration, without an account. Returns the monthly payment, fixed debit rate, fixed TAEG, total repaid and total interest, plus the market-average rate BoursoBank compares itself to. Car loans are the new_vehicle, used_vehicle and electric_vehicle projects; the electric project also returns the discounted eco-responsible rate granted once proof is validated. Each project has its own amount and duration bounds, which are returned and enforced: a request outside them fails with the allowed range.

- Site: boursobank.com
- Address: `reduck/boursobank.com/simulate-personal-loan`
- Updated: 2026-09-18 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/boursobank.com/simulate-personal-loan`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/boursobank.com/simulate-personal-loan
```

## Input

- `amount` (integer, required): Amount borrowed in euros, in steps of 500.
- `project` (string, required): What the loan finances. Bounds depend on it: used_vehicle caps at 30 000 € and 60 months, new_vehicle at 50 000 €, electric_vehicle at 75 000 € and 72 months, loan_buyback at 30 000 € (measured 2026-09).
- `duration` (integer, required): Repayment duration in months, in steps of 6.

## Output

- `url` (string, required)
- `taeg` (number, required): Fixed TAEG (annual percentage rate of charge), percent.
- `amount` (integer, required)
- `bounds` (object, required): Amount and duration range the site allows for this project.
- `project` (string, required)
- `debit_rate` (number, required): Fixed annual debit rate, percent.
- `total_repaid` (number, required): Total amount due over the loan, euros.
- `market_average` (object, required): The market benchmark BoursoBank shows next to its offer.
- `total_interest` (number, required): Total interest cost, euros.
- `duration_months` (integer, required)
- `eco_responsible` (object | null, required): Discounted terms granted once the eco-responsible proof is validated; null when the project is not eligible.
- `monthly_payment` (number, required): Monthly instalment in euros, excluding optional insurance.

## FAQ

### What does "Simulate a BoursoBank personal loan" do?

Run BoursoBank's personal loan simulator (prêt personnel) for a project type, an amount and a duration, without an account. Returns the monthly payment, fixed debit rate, fixed TAEG, total repaid and total interest, plus the market-average rate BoursoBank compares itself to. Car loans are the new_vehicle, used_vehicle and electric_vehicle projects; the electric project also returns the discounted eco-responsible rate granted once proof is validated. Each project has its own amount and duration bounds, which are returned and enforced: a request outside them fails with the allowed range.

### How do I automatically simulate a BoursoBank personal loan on boursobank.com?

Ask an AI agent connected to Reduck to run reduck/boursobank.com/simulate-personal-loan, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boursobank.com/simulate-personal-loan

### Is there a boursobank.com API to simulate a BoursoBank personal loan?

You do not need one. "Simulate a BoursoBank personal loan" drives the real boursobank.com pages in a browser, so it works whether or not boursobank.com offers an API for this.

### What information do I need to provide?

Required: project, amount, duration.

### What does it return?

It returns url, taeg, amount, bounds, project, debit_rate, total_repaid, market_average, total_interest, duration_months, eco_responsible, monthly_payment.

### Do I need to be logged in to boursobank.com?

No. It only uses pages of boursobank.com that are reachable without signing in.

### Does it change anything on boursobank.com, or only read data?

It only reads. It looks things up on boursobank.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/boursobank.com/simulate-personal-loan, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boursobank.com/simulate-personal-loan

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/boursobank.com/simulate-personal-loan
