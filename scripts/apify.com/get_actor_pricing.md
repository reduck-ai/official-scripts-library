# Get Apify actor pricing

Automatically get Apify actor pricing on apify.com. Get the pricing of one Apify Store actor, as its pricing page on apify.com shows it. Takes the actor id (owner/name, e.g. compass/crawler-google-places) or its apify.com URL. Returns the pricing model, then for a pay-per-event actor each chargeable event (title, description, whether it is the primary event or charged once per run) with its price in USD, either one price or one price per Apify plan tier (Free, Starter, Scale, Business, plus the unlisted Platinum and Diamond tiers). A FREE model means the actor itself costs nothing and only Apify platform usage is billed. Also returns the price changes Apify has announced for a later date, if any. Prices are per single event, in USD; the page shows them per 1,000. Fails with a clear message when the actor does not exist or is not public. Anonymous, read-only.

- Site: apify.com
- Address: `reduck/apify.com/get_actor_pricing`
- Updated: 2026-11-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/apify.com/get_actor_pricing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/apify.com/get_actor_pricing
```

## Input

- `actor` (string, required): The actor, as owner/name (compass/crawler-google-places), owner~name, or any apify.com URL of it (https://apify.com/compass/crawler-google-places/pricing). apify.com/search_actors returns it as actorId.

## Output

- `url` (string, required): The actor's pricing page on apify.com.
- `title` (string | null, required)
- `actorId` (string, required): owner/name.
- `current` (any, required): The pricing in effect now.
- `upcoming` (array, required): Pricing Apify has announced for a later date, soonest first. Empty when none.
- `isDeprecated` (boolean | null, optional)

## FAQ

### What does "Get Apify actor pricing" do?

Get the pricing of one Apify Store actor, as its pricing page on apify.com shows it. Takes the actor id (owner/name, e.g. compass/crawler-google-places) or its apify.com URL. Returns the pricing model, then for a pay-per-event actor each chargeable event (title, description, whether it is the primary event or charged once per run) with its price in USD, either one price or one price per Apify plan tier (Free, Starter, Scale, Business, plus the unlisted Platinum and Diamond tiers). A FREE model means the actor itself costs nothing and only Apify platform usage is billed. Also returns the price changes Apify has announced for a later date, if any. Prices are per single event, in USD; the page shows them per 1,000. Fails with a clear message when the actor does not exist or is not public. Anonymous, read-only.

### How do I automatically get Apify actor pricing on apify.com?

Ask an AI agent connected to Reduck to run reduck/apify.com/get_actor_pricing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apify.com/get_actor_pricing

### Is there a apify.com API to get Apify actor pricing?

You do not need one. "Get Apify actor pricing" drives the real apify.com pages in a browser, so it works whether or not apify.com offers an API for this.

### What information do I need to provide?

Required: actor.

### What does it return?

It returns url, title, actorId, current, upcoming, isDeprecated.

### Do I need to be logged in to apify.com?

No. It only uses pages of apify.com that are reachable without signing in.

### Does it change anything on apify.com, or only read data?

It only reads. It looks things up on apify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/apify.com/get_actor_pricing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apify.com/get_actor_pricing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/apify.com/get_actor_pricing
