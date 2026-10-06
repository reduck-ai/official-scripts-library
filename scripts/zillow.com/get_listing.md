# Get Zillow listing

Automatically get Zillow listing on zillow.com. Pass the ID from a home's Zillow URL and get its price, Zestimate, Rent Zestimate, size and listing agent.

- Site: zillow.com
- Address: `reduck/zillow.com/get_listing`
- Updated: 2026-10-05 (v6)
- Author: Reduck AI (reduck)

## About

Copy the number in front of _zpid in a Zillow home's URL, or take it from a single-home card in the search script's output. You get that page's figures as JSON, from the price, Zestimate and Rent Zestimate to year built, days on Zillow and the agent, plus lease term, pet policy and move-in date on rentals. Search cards carry price, beds, baths and area but neither estimate, which is what this call adds. Say you are screening three-bed houses in Columbus, Ohio. Pull a dozen zpids from search, run each one, multiply rentZestimate by 12, divide by price, and book tours only on the homes that clear a 7% gross yield. The catch is Zillow's PerimeterX "Press & Hold" check. Over the last two versions the hosted cloud browser was stopped by it all 7 times it tried, while the Reduck extension in people's own Chrome returned data in 95 of 97 runs.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zillow.com/get_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zillow.com/get_listing
```

## Input

- `zpid` (string, required): Zillow property id, as returned by the search script. The slug-less /homedetails/<zpid>_zpid/ URL redirects to the canonical page, so no address or slug is needed.

## FAQ

### What does "Get Zillow listing" do?

Fetch one Zillow property's full detail by zpid (from `search`): address, price, status/type, beds/baths/area, lot, year built, zestimates, geo, description, agent/broker, plus structured rental facts (leaseTerm, furnished, allowedPets, appliances, availabilityDate) — null on for-sale listings.

### How do I automatically get Zillow listing on zillow.com?

Ask an AI agent connected to Reduck to run reduck/zillow.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/get_listing

### Is there a zillow.com API to get Zillow listing?

You do not need one. "Get Zillow listing" drives the real zillow.com pages in a browser, so it works whether or not zillow.com offers an API for this.

### What information do I need to provide?

Required: zpid.

### Do I need to be logged in to zillow.com?

No. It only uses pages of zillow.com that are reachable without signing in.

### Does it change anything on zillow.com, or only read data?

It only reads. It looks things up on zillow.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zillow.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/get_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Why does it stop with a Press & Hold error?

That error means Zillow's PerimeterX "Press & Hold" check was still up after get_listing pressed and held it four times, a little longer on each try (6 seconds, then 8, 10 and 12). No listing was read, and the zpid itself is probably fine. The hosted cloud browser has hit this wall every time on record, so run it through the extension in your own Chrome, or in another browser on a home internet connection, and retry after a break.

### Does it return price history, tax records, HOA fees or photos?

The get_listing script returns the current price, zestimate, rentZestimate, pricePerSquareFoot, daysOnZillow and a photoCount, but not the price or tax history tables, HOA fees, school ratings or any image URLs. If the home came out of a zillow.com search run, its card there already carries the main photo as imgSrc.

### What extra details come back for a rental listing?

On Zillow rentals, get_listing also fills leaseTerm, furnished, allowedPets, appliances and availabilityDate from the page's Facts and features section. Two more fields help before you reach out: rentalApplicationsAcceptedType names the apply option the listing offers (for example REQUEST_TO_APPLY or APPLY_NOW), and isRentalsLeadCapMet, going by its name, flags a rental that has reached its cap on leads. On homes for sale all of these come back null.

### Can I get Zestimates straight from Zillow instead?

Zillow Group has a Zestimates API, but its developer page says it is meant for commercial use by businesses, access starts with a request form, and no price is published. Academic and research projects are pointed to Zillow's research data downloads instead, which give typical values for ZIP codes, cities and metros rather than numbers for one house. For checking a dozen homes you might buy, that application is a lot of process.

Source: https://reduck.ai/explore/scripts/reduck/zillow.com/get_listing
