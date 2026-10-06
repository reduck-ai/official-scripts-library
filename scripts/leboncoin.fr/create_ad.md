# Create a leboncoin classified ad

Automatically create a leboncoin classified ad on leboncoin.fr. Create a classified ad on leboncoin from a title, description, price and category. Defaults to a dry run that fills the form and reports what would be posted without publishing; pass dryRun false to actually publish.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/create_ad`
- Updated: 2026-10-05 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/create_ad`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/create_ad
```

## Input

- `photo` (string, required): The ad photo (PNG or JPEG). leboncoin refuses to publish an ad with no photo.
- `price` (number, required): Asking price in euros.
- `title` (string, required): Ad title. leboncoin derives the category suggestions from this, so it must describe the item (e.g. "Vélo de ville adulte").
- `lastName` (string, required): Seller last name, required by the form.
- `location` (string, required): Street address to advertise from, e.g. "12 rue Duphot Paris". Resolved against leboncoin's own address suggestions; the first suggestion is taken and returned in resolvedLocation.
- `firstName` (string, required): Seller first name, required by the form.
- `description` (string, required): Ad body text.
- `dryRun` (boolean, optional): True (default) fills and validates the whole form, including resolving the address, reports what would be posted, and stops before submitting, so no ad is created. Set false to actually publish (free option only). The boost and free-option steps after submitting only run on a real publish.

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

Required: title, description, price, location, firstName, lastName, photo. Optional: dryRun.

### What does it return?

It returns price, title, dryRun, published, categoryChosen, confirmationText, resolvedLocation.

### Do I need to be logged in to leboncoin.fr?

Yes. It acts as you on leboncoin.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the leboncoin.fr cookies saved by the Reduck extension.

### Does it change anything on leboncoin.fr, or only read data?

It makes changes on leboncoin.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/create_ad, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/create_ad

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/create_ad
