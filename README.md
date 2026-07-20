# Jose & Gladis — Wedding Invitation Site

A fully self-contained wedding invitation website for Jose & Gladis, August 29, 2026.

## Features

- Animated envelope landing screen with starfield, floating petals, and zoom-into-site transition
- Hero section with script-font names and floral SVG accents
- Live countdown timer to the wedding date
- Announcement box with parents' names and padrinos
- Event details (ceremony + reception)
- Damas de Honor listing
- RSVP form via [Formspree](https://formspree.io)
- Fully responsive — mobile-first layout down to ~375px

## Deployment

### GitHub Pages (recommended)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/`

### Any static host

Just upload `index.html` — no build step, no dependencies, no server required.

## Customization

All content is in `index.html`. Key things to update:

| What | Where in the file |
|------|-------------------|
| RSVP form endpoint | `fetch('https://formspree.io/f/mgobdjvn', …)` |
| Wedding date/time | `new Date('2026-08-29T16:00:00')` in the countdown script |
| Ceremony address | `.detail-sub` under `detail-type` "Ceremonia" |
| Reception address | `.detail-sub` under `detail-type` "Recepción" |
| Parents' names | `.parents-name` divs in the `#announcement` section |
| Damas de Honor | `<p>` inside `#damas` section |

## Stack

- Vanilla HTML/CSS/JS — zero frameworks, zero build tools
- Fonts: [Cormorant Garamond](https://fonts.google.com/specimen/Cormorant+Garamond), [Pinyon Script](https://fonts.google.com/specimen/Pinyon+Script), [Jost](https://fonts.google.com/specimen/Jost) via Google Fonts
- RSVP backend: [Formspree](https://formspree.io)
