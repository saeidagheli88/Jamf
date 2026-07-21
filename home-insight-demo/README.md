# HomeInsight — Demo

A working prototype of a "one-page neighborhood report" for people buying or
renting a home. Type in an address (or pick a sample home) and see everything
that matters in one place — instead of juggling a dozen browser tabs.

## What it shows

Two modes, switchable at the top:

- **One home** — look up a single address and see its full report.
- **Compare two** — put two homes side by side and see which one wins each
  category (price, schools, errands, walkability, safety), with the stronger
  value in every row highlighted.

For each home, a single scannable report:

- **Overall fit score** — a quick at-a-glance rating
- **Price check** — the home's price vs. the area median, plus price per sq ft
- **Schools nearby** — ratings and distances
- **Everyday errands** — drive distance/time to Costco, Walmart, and grocery
- **Getting around** — walk / transit / bike scores and nearby amenity counts
- **Neighborhood safety** — an official-source summary, framed responsibly

## Run it

It's a single self-contained HTML file — no build step, no dependencies.

```
open home-insight-demo/index.html      # macOS
# or just double-click the file
```

## Status: demo / sample data

The three homes are **made-up sample data** to show the experience. A real
product would pull live prices, schools, and map data from licensed sources
(e.g. an MLS/listings feed, a schools API, and a maps/places API).

### A note on the safety feature

Housing safety data is sensitive and, in the U.S., interacts with Fair Housing
law. This demo deliberately shows a responsibly-framed, official-source summary
rather than raw crime figures. Any real version should follow the same approach
and get a legal review before launch.

## Meant to become its own project

This lives in a folder for now, but it's fully self-contained and intended to be
moved into its own repository when the project moves past the demo stage.
