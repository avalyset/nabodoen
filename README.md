# Nabodo

**Open your door. Find a neighbour.**

Nabodo is a hyperlocal platform for Oslo where residents open their homes to
people nearby — a toilet when you're caught out, a phone charge, a refill of
water, a place to warm baby food. It runs on reciprocity — you give to get.
Micro-hospitality, not a utility finder.

The idea was first floated on air by «Kokke Øyvind» on NRK Stor-Oslo in April
2026, and built out from there.

Live at → **[nabodo.no](https://nabodo.no)**

---

## About this repository

This repo holds the **Nabodo web front-end** — the public site at nabodo.no.
It is a single `index.html` with inline CSS and JavaScript, a service worker,
and a web app manifest. No build step, no dependencies: clone it and open the
file.

The platform logic — accounts, bookings, the reciprocity ledger, payments —
runs server-side and is **not part of this repository**. That split is
deliberate: the front-end is open to read, study, and improve via pull request;
the service layer stays closed. See [LICENSE](LICENSE).

---

## What's in here

- The full nabodo.no single-page site (`index.html`)
- A custom CSS design system: 8px spacing grid, consistent card and radius
  tokens, no framework
- Leaflet map with OpenStreetMap tiles and live public-amenity layers
- Progressive web app scaffolding (`manifest.json`, `sw.js`, icons)
- Norwegian-language UI throughout

---

## The idea, briefly

Nabodo is organised in tiers, from free community access up to paid
experiences. The free tier is the heart of it; everything above is optional.

| Tier | Type | Example |
|------|------|---------|
| 0 | Free community access | Toilet, water, charging, baby-changing |
| 1 | Micro-rental | Power bank, umbrella, kayak, skis |
| 2 | Micro-services | Errands, small fixes, gardening |
| 3 | Experiences | Guitar lesson, sailing trip, coaching |

The reciprocity rule is the core identity, not a feature: to use what
neighbours offer, you register as a host yourself. Goodwill is tracked so the
exchange stays balanced.

> The host profiles and activity shown on the live site are demonstration
> data. Nabodo is in early beta.

---

## Tech

| Part | Choice |
|------|--------|
| Front-end | One `index.html`, no build step |
| Maps | Leaflet + OpenStreetMap |
| PWA | `manifest.json` + service worker |
| Hosting | Cloudflare Pages |

---

## Contributing

Contributions to the front-end are welcome — see
[CONTRIBUTING](CONTRIBUTING.md). Good places to start: mobile accessibility,
English translation of the UI, and map improvements.

---

## Owner

**EcoDeco AS** · Org.nr. 936 320 856
Founder: Eirik Botten Nicolaysen

Built with the help of AI coding tools; all decisions, architecture, and
ownership are the founder's.

---

## License

Source Available — see [LICENSE](LICENSE). This is **not** open source: you may
read, study, and contribute back, but not copy, sell, or launch a competing
service. Nabodo® is a trademark of EcoDeco AS.
