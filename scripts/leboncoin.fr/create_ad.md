# Create a leboncoin classified ad

Automatically create a leboncoin classified ad on leboncoin.fr. Create a classified ad on leboncoin from a title, description, price and category. Defaults to a dry run that fills the form and reports what would be posted without publishing; pass dryRun false to actually publish.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/create_ad`
- Updated: 2026-09-22 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/create_ad`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/create_ad
```

## Input

- `price` (number, required): Asking price in euros.
- `title` (string, required): Ad title. leboncoin derives the category suggestions from this, so it must describe the item (e.g. "Vélo de ville adulte").
- `lastName` (string, required): Seller last name, required by the form.
- `location` (string, required): Street address to advertise from, e.g. "12 rue Duphot Paris". Resolved against leboncoin's own address suggestions; the first suggestion is taken and returned in resolvedLocation.
- `firstName` (string, required): Seller first name, required by the form.
- `description` (string, required): Ad body text.
- `imageBase64` (string, required): The ad photo as base64 (PNG or JPEG), without a data: prefix. leboncoin refuses to publish an ad with no photo.
- `dryRun` (boolean, optional): True (default) fills and validates the entire form — including resolving the address against leboncoin's own suggestions — reads back what would be posted, and returns without submitting, so no ad is created. Set false to actually publish, which takes the free option only. Note what a truthful dry run costs: the ad is created by the form submit itself, not by the later publish-looking button, so a dry run cannot exercise anything past the submit — the boost step and the free-option handling are only covered by a real publish. Do not move this gate later to buy that coverage: an earlier version submitted first and reported published:false, leaving a real, live classified ad on the account every single time.

## Output

- `title` (string, required)
- `dryRun` (boolean, required)
- `published` (boolean, required): True only when the confirmation screen was reached. False on a dry run.
- `categoryChosen` (string, required): The category leboncoin suggested for this title and the script selected.
- `resolvedLocation` (string, required): The address as leboncoin resolved it from its own suggestions, e.g. "12 Rue Duphot, Paris (75001)".
- `price` (number | null, optional)
- `confirmationText` (string | null, optional): The confirmation screen's message when published; null on a dry run. A newly posted ad sits at "En cours de vérification" until leboncoin reviews it.

## FAQ

### What does "Create a leboncoin classified ad" do?

Create a classified ad on leboncoin from a title, description, price and category. Defaults to a dry run that fills the form and reports what would be posted without publishing; pass dryRun false to actually publish.

### How do I automatically create a leboncoin classified ad on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/create_ad, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/create_ad

### Is there a leboncoin.fr API to create a leboncoin classified ad?

You do not need one. "Create a leboncoin classified ad" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Required: title, description, price, location, firstName, lastName, imageBase64. Optional: dryRun.

### What does it return?

It returns price, title, dryRun, published, categoryChosen, confirmationText, resolvedLocation.

### Do I need to be logged in to leboncoin.fr?

Yes. It acts as you on leboncoin.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the leboncoin.fr cookies saved by the Reduck extension.

### Does it change anything on leboncoin.fr, or only read data?

It makes changes on leboncoin.fr, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/create_ad, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/create_ad

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/create_ad
