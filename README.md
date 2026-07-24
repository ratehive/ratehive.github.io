# Ratehive

A free toolkit for creators working with brands: price a deal, track it to payment,
and generate a rate card worth sending.

**Live:** https://ratehive.github.io/

## What it does

- **Rate calculator** — blends a per-view CPM model with an audience-size floor, then
  adjusts for deliverable type, usage rights, and exclusivity.
- **Deal tracker** — pipeline from inquiry to paid, with totals and overdue flags.
- **Rate card generator** — plain-text card to paste into an email or media kit.

## How it's built

One file. `index.html` is the entire application — no build step, no dependencies to
install, no backend. Deal data is written to `localStorage`, so it survives a refresh
but never leaves the device; there is no server to send it to.

To work on it locally:

```sh
python3 -m http.server 8788
# then open http://127.0.0.1:8788/
```

Deployment is GitHub Pages off the `main` branch, so pushing to `main` publishes.

## Notes on the rate numbers

The CPM table in `index.html` is a set of benchmark assumptions, not measured data.
They are a starting anchor for negotiation and are expected to be revised as real
creators report what their deals actually paid.
