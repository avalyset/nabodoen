# Nabodo

**Nabolaget som hjelper hverandre.**

Nabodo er en hyperlokal mikrotjeneste- og mikro-utleiemarkedsplass der naboer er både tilbydere og brukere. Ingen er bare konsument — alle bidrar for å delta.

> "Glemte du paraplyen på do? Bra vi har Nabodo."

Live på → **[nabodo.no](https://nabodo.no)**
Omtalt på → NRK Stor-Oslo, april 2026

---

## Status — v4.7.3 (april 2026)

| Komponent | Status |
|-----------|--------|
| **nabodo.no** | Live — Cloudflare Pages |
| **nabodo-api.ecodeco.workers.dev** | Live — Cloudflare Workers + Hono |
| **D1 database** | 16 tabeller, 60 katalogposter, 48 verter (46 aktive) |
| **Stripe Connect** | Sandbox — konto opprettet, webhook verifisert |
| **Vipps Login + eCom** | Under godkjenning (~1 uke fra 11. april) |
| **Crisp + Hugo AI** | Live — 8 FAQ-artikler, auto-crawl |
| **Cron triggers** | 4 aktive (auto-complete, påminnelser, ukesrapport, månedsrapport) |

---

## Hva fungerer nå

- 60 tjenester i katalogen (4 lag, 4 sesonger, inkl. grill/mat-opplevelser)
- Tier-system: Nabo → Stamgjest → Nabovert → SuperNabo (cron-automasjon)
- CSS designsystem: 8px grid, 5 radii-verdier, konsistent kort-DNA
- Komplett booking-livssyklus: request → confirm → deliver (QR) → complete
- Blind toveis-rating med auto-publisering
- GVP-system (God Vilje Poeng) med immutable ledger
- Anti-fluff deteksjon (5 sjekker, logging)
- Anti-disintermediation (chat-filter, vilkår)
- Anti-misbruk (illegal keywords, misuse reports, Slack-varsling)
- Rapporter misbruk-knapp i vertprofiler
- Stripe PaymentIntent med 85/15 split
- QR-leveringsbekreftelse med engangskode (UUID, TTL 2t)
- Auto-godkjenning etter 2 timer (cron)
- Kvitteringer via MailChannels
- DAC7-rapport for Skatteetaten
- Sesongfilter (vår, sommer, vinter)
- GPS-privatliv (avrundede koordinater for uautentiserte)

---

## Produktlag

| Lag | Type | Provisjon |
|-----|------|-----------|
| 0 | Gratis (toalett, vann, lading, stellerom) | 0 % — kun GVP |
| 1 | Mikro-utleie (powerbank, paraply, kajakk, ski) | 15 % |
| 2 | Mikro-tjenester (innkjøp, småfiks, hagearbeid) | 15 % |
| 3 | Opplevelser (gitartime, DJ, seiltur, coaching) | 12 % |

---

## Tech stack

| Komponent | Løsning |
|-----------|---------|
| Frontend | Én `index.html`, ingen build-steg, Leaflet + Windy |
| API | Cloudflare Workers, Hono framework, TypeScript |
| Database | Cloudflare D1 (SQLite), 16 tabeller |
| Betaling | Stripe Connect (sandbox) + Vipps eCom (under godkjenning) |
| Auth | Dev stub (bølge 0) → Vipps OIDC (bølge 1) |
| E-post | MailChannels (kvitteringer, rating-prompts, månedsrapporter) |
| Chat | Crisp med Hugo AI-agent |
| Deploy | `wrangler pages deploy` (frontend), `wrangler deploy` (API) |

---

## Booking-livssyklus

```
requested → confirmed (vert bekrefter)
confirmed → delivered (vert leverer, QR-kode genereres)
delivered → completed (gjest godkjenner, eller auto etter 2t)
confirmed → cancelled (auto etter 2t uten levering)
completed → rating-prompts sendt til begge parter
```

---

## Eier

**EcoDeco AS** · Org.nr. 936 320 856
Grunder: Eirik Botten Nicolaysen

---

## Lisens

Source Available — se [LICENSE](LICENSE). Ikke open source.
