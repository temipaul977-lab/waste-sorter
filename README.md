# Where does this go?

A phone-friendly tool that tells you which stream a piece of household waste belongs to —
and where in Ilorin you can take it.

**Live demo:** https://temipaul977-lab.github.io/waste-sorter/

## The problem

In Ilorin, recyclable material moves wherever a buyer exists. Bottles carry a crate
deposit at the distributor, tins and aluminium have a purchaser, copper wire gets
stripped and sold. Plastic film does not — so sachet water nylon is dumped, burned,
or buried.

The distinction that decides whether a collector's load sells or gets rejected is
exactly the distinction households do not make: PET bottle versus sachet film. Both
look like "plastic", only one has a buyer, and mixing them downgrades or spoils the
bale. Mixed scrap is priced at its cheapest material, and a single contaminated item
can cost a collector the whole bag.

## What it does

Search an item → get the stream (buy-back, general bin, organic, reuse, or special
drop-off), the prep steps that decide whether it sells, and where to take it in Ilorin.

It answers to the words people actually use: `rubber`, `pure water`, `keg`,
`evabottle`, `okrika`, `iron`.

When there is no verified buyer for a material, the tool says so instead of inventing
one. Sachet nylon has no confirmed small-quantity buyer in Ilorin, and the app tells
users that rather than sending them on a wasted journey.

## How it works

One HTML file. No frameworks, no build step, no server, no accounts.

- Items are an array of objects (`name`, `stream`, `steps`, `where`, `searchWords`)
- A function filters the array on every keystroke and redraws the cards
- Search matches against the item name plus a list of local synonyms
- Hosted free on GitHub Pages

## Run it locally

Download `index.html` and open it in any browser. That's the whole installation.

## Data and sources

| What | Status |
|---|---|
| Item taxonomy and disposal rules | Drafted from published recycling guidance, adapted for Lagos/Ilorin practice |
| Buy-back points | Public listings checked 20 Oct 2026 — **not visited or called** |
| Prices | **Not shown in the app.** Web estimates only, from non-Ilorin yards |
| Field verification | **None.** No interviews, calls or site visits were conducted for this build |

### What this project does not claim

Stating the limits plainly, because they matter more than the claims:

- No buy-back point has been visited or called, so no price is shown anywhere in the app
- No interviews were conducted; the problem statement is built from published sources
  and general knowledge of how informal recycling works in Lagos and Ilorin
- No verified e-waste drop-off exists in Ilorin in this dataset
- Sachet nylon's buyer situation is unconfirmed and described as unconfirmed
- The tool is not a substitute for asking the yard you intend to visit

## What's next

1. Call and visit the buy-back points; replace every estimate with a confirmed price and date
2. Add the camera, so an item can be identified from a photo instead of a search
3. Measure accuracy on held-out local photos and publish the number
4. Test with real households and record whether they reach the correct disposal action

## Built for

Arbiter Hacks V1 — Theme Track, Rethinking Waste.

## Licence

MIT
