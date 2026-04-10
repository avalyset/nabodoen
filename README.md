# 🚪 Nabodo

**Åpne din dør. Finn en nabo.**

> «Fordi alle har vært der.»

Live på → **[nabodo.no](https://nabodo.no)**  
Omtalt på → NRK Stor-Oslo, april 2026

---

## Hva er Nabodo?

Nabodo er en **1:1-tjeneste** — du registrerer deg som vert og får tilgang til alle andre verter nær deg. Gjensidig tillit er selve mekanismen. Ingen anonyme gjester, ingen enveisbruk. Du gir en dør — du får tilgang til hundrevis.

Oslo har systematisk for få offentlige toaletter i boligstrøk. Nabodo løser dette nedenfra — én dør om gangen.

---

## Modellen

Nabodo er ikke bare et toalettnettverk. Verter kan tilby:

🚽 Toalett · 🔋 Lading · 🧊 Kjøl medbrakt drikke · 🚰 Fyll vannflaske  
☀️ Nødsolkrem · 🌂 Nødparaply · 📚 Lån en bok · 🎸 Lån en gitar  
🛋️ Lån et pledd · 🏸 Lån badminton · ⚽ Bli med å spille  
🍼 Varme barnemat/melk · 🩺 Kan førstehjelp · 💗 Hjertestarter  
👋 Bli med på kaffe · 🎵 Musikk og stemning

---

## Status

```
v1.5.3 — Beta
✅ nabodo.no live på Cloudflare Pages
✅ PWA — installer fra nettleseren
✅ 34 mockup-verter i Oslo sentrum
✅ Interaktive profiler med filter og søk
✅ Nabo søker nabo-feed
✅ Nabodo-score og statistikk
✅ Formspree e-post-registrering
✅ Personvern + vilkår (GDPR)
✅ Åpen kildekode på GitHub
🔜 BankID-innlogging (mai 2026)
🔜 Cloudflare Workers + D1 database
🔜 Kartverket kart og geolokasjon
🔜 Vipps-integrasjon
🔜 Toveisratings
```

---

## Teknologi

| Komponent | Løsning |
|-----------|---------|
| Frontend | HTML/CSS/JS |
| Hosting | Cloudflare Pages |
| PWA | manifest.json + service worker |
| Skjema | Formspree |
| Backend (fase 2) | Cloudflare Workers + D1 |
| Auth (fase 2) | BankID via Criipto |
| Kart (fase 2) | Kartverket API |
| Betaling (fase 2) | Vipps |

---

## Kom i gang

```bash
git clone https://github.com/nabodo/nabodoen.git
cd nabodoen
open index.html
```

Ingen avhengigheter. Bare åpne `index.html` i nettleseren.

---

## Bidra

- 🐛 **Bugfixes** — finn og fiks feil
- 💡 **Funksjoner** — foreslå via Issues
- 🎨 **Design** — forbedre UI/UX
- 🗺️ **Kart** — Kartverket-integrasjon
- 🔐 **Sikkerhet** — BankID og GDPR

### Slik bidrar du

1. Fork repo-en
2. Lag en branch: `git checkout -b min-funksjon`
3. Commit: `git commit -m "feat: legg til X"`
4. Push og åpne en Pull Request

Se [CONTRIBUTING.md](CONTRIBUTING.md) for detaljer.

---

## Sommerdugnad 2026

Vi jobber mot **1000 registrerte verter i Oslo innen 1. august 2026** — i samarbeid med NRK Stor-Oslo.

Vil du være med? Meld deg på [nabodo.no](https://nabodo.no) eller bidra her på GitHub.

---

## Eier

**EcoDeco AS** · Org.nr. 936 320 856  
Grunder: Eirik Botten Nicolaysen

---

## Lisens

MIT — bruk fritt, gi gjerne kreditt.
